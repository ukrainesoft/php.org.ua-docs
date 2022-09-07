---
navigation:
  - eventbufferevent.sslerror.md: '« EventBufferEvent::sslError'
  - eventbufferevent.sslgetcipherinfo.md: 'EventBufferEvent::sslGetCipherInfo »'
  - index.md: PHP Manual
  - class.eventbufferevent.md: EventBufferEvent
title: 'EventBufferEvent::sslFilter'
---
# EventBufferEvent::sslFilter

(PECL event >= 1.2.6-beta)

EventBufferEvent::sslFilter — Створює нову подію буфера SSL для надсилання своїх даних через іншу подію буфера

### Опис

```methodsynopsis
public
   static
   EventBufferEvent::sslFilter(    
    EventBase
     $base
   ,    
    EventBufferEvent
     $underlying
   ,    
    EventSslContext
     $ctx
   ,    
    int
     $state
   ,    
    int
     $options
     = 0
   ): EventBufferEvent
```

Створює нову подію буфера SSL для надсилання своїх даних через іншу подію буфера

> **Зауваження**
> 
> Функція доступна лише в тому випадку, якщо `Event` скомпільований за допомогою OpenSSL.

### Список параметрів

`base`

Пов'язана основа подій.

`underlying`

Подія буфера сокету використовувати для цього SSL.

`ctx`

Об'єкт класу [EventSslContext](class.eventsslcontext.md)

`state`

Поточний стан SSL-з'єднання: **`EventBufferEvent::SSL_OPEN`** **`EventBufferEvent::SSL_ACCEPTING`** або **`EventBufferEvent::SSL_CONNECTING`**

`options`

Один чи кілька параметрів буфера.

### Значення, що повертаються

Повертає новий SSL [EventBufferEvent](class.eventbufferevent.md) об'єкт.

### Приклади

**Приклад #1 Простий SMTP-сервер**

```php
<?php
 /*
 * Автор: Andrew Rose <hello at andrewrose dot co dot uk>
 *
 * Usage:
 * 1) Подготовим файлы сертификата cert.pem и приватного ключа privkey.pem.
 * 2) Запустим скрипт сервера
 * 3) Откроем TLS-соединение, например:
 *      $ openssl s_client -connect localhost:25 -starttls smtp -crlf
 * 4) Протестируем команды, описанные в метода `cmd`.
 */

class Handler {
    public $domainName = FALSE;
    public $connections = [];
    public $buffers = [];
    public $maxRead = 256000;

    public function __construct() {
        $this->ctx = new EventSslContext(EventSslContext::SSLv3_SERVER_METHOD, [
            EventSslContext::OPT_LOCAL_CERT  => 'cert.pem',
            EventSslContext::OPT_LOCAL_PK    => 'privkey.pem',
            //EventSslContext::OPT_PASSPHRASE  => '',
            EventSslContext::OPT_VERIFY_PEER => false, // для корректного сертификата укажите true
            EventSslContext::OPT_ALLOW_SELF_SIGNED => true // для корректного сертификата укажите false
        ]);

        $this->base = new EventBase();
        if (!$this->base) {
            exit("Не удалось открыть обработчик событий\n");
        }

        if (!$this->listener = new EventListener($this->base,
            [$this, 'ev_accept'],
            $this->ctx,
            EventListener::OPT_CLOSE_ON_FREE | EventListener::OPT_REUSEABLE,
            -1,
            '0.0.0.0:25'))
        {
            exit("Невозможно создать слушателя\n");
        }

        $this->listener->setErrorCallback([$this, 'ev_error']);
        $this->base->dispatch();
    }

    public function ev_accept($listener, $fd, $address, $ctx) {
        static $id = 0;
        $id += 1;

        $this->connections[$id]['clientData'] = '';
        $this->connections[$id]['cnx'] = new EventBufferEvent($this->base, $fd,
            EventBufferEvent::OPT_CLOSE_ON_FREE);

        if (!$this->connections[$id]['cnx']) {
            echo "Failed creating buffer\n";
            $this->base->exit(NULL);
            exit(1);
        }

        $this->connections[$id]['cnx']->setCallbacks([$this, "ev_read"], NULL,
            [$this, 'ev_error'], $id);
        $this->connections[$id]['cnx']->enable(Event::READ | Event::WRITE);

        $this->ev_write($id, '220 '.$this->domainName." wazzzap?\r\n");
    }

    function ev_error($listener, $ctx) {
        $errno = EventUtil::getLastSocketErrno();

        fprintf(STDERR, "Ошибка слушателя: %d (%s). Аварийное завершение работы.\n",
            $errno, EventUtil::getLastSocketError());

        if ($errno != 0) {
            $this->base->exit(NULL);
            exit();
        }
    }

    public function ev_close($id) {
        $this->connections[$id]['cnx']->disable(Event::READ | Event::WRITE);
        unset($this->connections[$id]);
    }

    protected function ev_write($id, $string) {
        echo 'S('.$id.'): '.$string;
        $this->connections[$id]['cnx']->write($string);
    }

    public function ev_read($buffer, $id) {
        while($buffer->input->length > 0) {
            $this->connections[$id]['clientData'] .= $buffer->input->read($this->maxRead);
            $clientDataLen = strlen($this->connections[$id]['clientData']);

            if($this->connections[$id]['clientData'][$clientDataLen-1] == "\n"
                && $this->connections[$id]['clientData'][$clientDataLen-2] == "\r")
            {
                // удаляем все завершающие \r\n
                $line = substr($this->connections[$id]['clientData'], 0,
                    strlen($this->connections[$id]['clientData']) - 2);

                $this->connections[$id]['clientData'] = '';
                $this->cmd($buffer, $id, $line);
            }
        }
    }

    protected function cmd($buffer, $id, $line) {
        switch ($line) {
            case strncmp('EHLO ', $line, 4):
                $this->ev_write($id, "250-STARTTLS\r\n");
                $this->ev_write($id, "250 OK ehlo\r\n");
                break;

            case strncmp('HELO ', $line, 4):
                $this->ev_write($id, "250-STARTTLS\r\n");
                $this->ev_write($id, "250 OK helo\r\n");
                break;

            case strncmp('QUIT', $line, 3):
                $this->ev_write($id, "250 OK quit\r\n");
                $this->ev_close($id);
                break;

            case strncmp('STARTTLS', $line, 3):
                $this->ev_write($id, "220 Ready to start TLS\r\n");
                $this->connections[$id]['cnx'] = EventBufferEvent::sslFilter($this->base,
                    $this->connections[$id]['cnx'], $this->ctx,
                    EventBufferEvent::SSL_ACCEPTING,
                    EventBufferEvent::OPT_CLOSE_ON_FREE);
                $this->connections[$id]['cnx']->setCallbacks([$this, "ev_read"], NULL, [$this, 'ev_error'], $id);
                $this->connections[$id]['cnx']->enable(Event::READ | Event::WRITE);
                break;

            default:
                echo 'неизвестная команда: '.$line."\n";
                break;
        }
    }
}

new Handler();
```

### Дивіться також

-   [EventBufferEvent::sslSocket()](eventbufferevent.sslsocket.md) - Створює нову буферну подію SSL для надсилання своїх даних через SSL у сокет
