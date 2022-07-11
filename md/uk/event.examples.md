- [« Типи ресурсів](event.resources.md)
- [Прапори подій »](event.flags.md)

- [PHP Manual](index.md)
- [Event](book.event.md)
- Приклади

# Приклади

**Приклад #1 Простий клієнт HTTP**

` <?php// Функція зворотного дзвінка обробки читанняfunction readcb($bev, $base) {    //$input = $bev->input; //$bev->getInput(); //$pos = $input->search("TTP"); $pos = $bev->input->search("TTP"); while(($n = $bev->input->remove($buf, 1024)) > 0) {        echo $buf; }}// Функція зворотного виклику обробки подіїfunction eventcb($bev, $events, $base) {    if ($events & EventBufferEvent::CONNECTED)                
";    } elseif ($events & (EventBufferEvent::ERROR | EventBufferEvent::EOF)) {        if ($events & EventBufferEvent::ERROR) {            echo "Ошибка DNS: ", $bev->getDnsErrorString(), PHP_EOL;        } echo "Закриваємо з'єднання
";        $base->exit();        exit("Готово
");    }}if ($argc != 3) {    echo <<<EOSTrivial HTTP 0.x clientSyntax: php {$argv[0]} [hostname] [$source| .google.com /EOS;   exit();}$base = new EventBase();$dns_base = new EventDnsBase($base, TRUE); // Використовуємо асинхронний d s  init DNS Base
");}$bev = new EventBufferEvent($base, /* используем внутренний сокет */ NULL,    EventBufferEvent::OPT_CLOSE_ON_FREE | EventBufferEvent::OPT_DEFER_CALLBACKS,    "readcb", /* writecb */ NULL, "eventcb");if ( !$bev) {   exit("Помилка створення сокету bufferevent
");}//$bev->setCallbacks("readcb", /* writecb */ NULL, "eventcb", $base);$bev->enable(Event::READ | Event::WRITE);$output = $bev->output; //$bev->getOutput();if (!$output->add(   "GET {$argv[2]} HTTP/1.0
".    "Host: {$argv[1]}
".    "Connection: Close

")) {   exit("Помилка додавання запиту в буфер висновку
");}if(!$bev->connectHost($dns_base, $argv[1], 80, EventUtil::AF_UNSPEC)) {    exit("Неможливо встановити з'єднання с {$argv[1]}
");}$base->dispatch();?> `

Результатом виконання цього прикладу буде щось подібне:

З'єднання встановлено.
HTTP/1.1 301 Moved Permanently
Date: Fri, 01 Mar 2013 18:47:48 GMT
Location: http://www.google.co.uk/
Content-Type: text/html; charset=UTF-8
Cache-Control: public, max-age=2592000
Server: gws
Content-Length: 221
X-XSS-Protection: 1; mode=block
X-Frame-Options: SAMEORIGIN
Age: 133438
Expires: Sat, 30 Mar 2013 05:39:28 GMT
Connection: close

<HTML><HEAD><meta http-equiv="content-type" content="text/html;charset=utf-8">
<TITLE>301 Moved</TITLE></HEAD><BODY>
<H1>301 Moved</H1>
The document has moved
<A HREF="http://www.google.co.uk/">here</A>.
</BODY></HTML>
Закриваємо з'єднання
Готово

**Приклад #2 HTTP клієнт з асинхронним запитом до DNS**

`<?php/* * 1. З'єднуємось з 127.0.0.1 на порту 80 * за допомогою EventBufferEvent::connect(). * * 2. Запрошуємо /index.cphp по протоколу HTTP/1.0 * використовуючи буфер висновку. * * 3. Асинхорнно читаємо відповідь і виводимо його в stdout. */// Функція зворотного дзвінка обробки читанняfunction readcb($bev, $base) {    $input = $bev->getInput(); while(($n = $input->remove($buf, 1024)) > 0) {       echo $buf; }}// Функція зворотного виклику обробки подіїfunction eventcb($bev, $events, $base) {    if ($events & EventBufferEvent::CONNECTED)                
";    } elseif ($events & (EventBufferEvent::ERROR | EventBufferEvent::EOF)) {        if ($events & EventBufferEvent::ERROR) {            echo "Ошибка DNS: ", $bev->getDnsErrorString(), PHP_EOL;        } echo "Закриваємо з'єднання
";        $base->exit();        exit("Готово
");    }}$base = new EventBase();echo "step 1
";$bev = new EventBufferEvent($base, /* використовуємо внутрішній сокет*/ NULL,   EventBufferEvent::OPT_CLOSE_ON_FREE | EventBufferEvent::OPT_DEFER_CALLBACK |
");}echo "step 2
";$bev->setCallbacks("readcb", /* writecb */ NULL, "eventcb", $base);$bev->enable(Event::READ||Event::WRITE);echo step 3
";// Посилаємо запит$output = $bev->getOutput();if (!$output->add(    "GET /index.cphp HTTP/1.0
".    "Connection: Close

")) {   exit("Помилка додавання запиту в буфер висновку
");}/* Синхронно з'єднуємось з хостом.Ми знаємо IP і не не маємо потребу в запиті к DNS.
");}// Обробляємо очікуючі події$base->dispatch();?> `

**Приклад #3 Ехо-сервер**

` <?php/* * Простой эхо-сервер на базе слушателя соединений libevent * * Использование: * 1) В первом терминальном окне запускаем: * * $ php listener.php 9881 * * 2) Во втором терминальном окне открываем соединение: * * $ nc 127.0.0.1 9881 * * 3) Починаємо друкувати. Сервер повинен повторювати наш введення. */class MyListenerConnection {    private $bev, $base; public function __destruct() {         $this->bev->free(); }    public function __construct($base, $fd) {        $this->base = $base; $this->bev = new EventBufferEvent($base, $fd, EventBufferEvent::OPT_CLOSE_ON_FREE); $this->bev->setCallbacks(array($this, "echoReadCallback"), NULL,            array($this, "echoEventCallback"), NULL); if (!$this->bev->enable(Event::READ)) {            echo "Не удалося дозволити читання (READ)
";            return;        }    }    public function echoReadCallback($bev, $ctx) {        // Копируем все данные из буфера ввода в буфер вывода        // Вариант #1        $bev->output->addBuffer($bev->input);        / * Вариант #2 */        /*        $input    = $bev->getInput();        $output = $bev->getOutput();        $output->addBuffer($input);        */    }    public function echoEventCallback($bev, $events, $ctx) {        if ($events & EventBufferEvent::ERROR) {            echo "Помилка bufferevent
";        }        if ($events & (EventBufferEvent::EOF | EventBufferEvent::ERROR)) {            //$bev->free();            $this->__destruct();        }    }}class MyListener {    public $base,        $ listener,        $socket;    private $conn = array();    public function __destruct() {        foreach ($this->conn as &$c) $c = NULL;    }    public function __construct($port) {        $this->base = new EventBase();        if (!$this->base) {            echo "Не удаётся создать EventBase";            exit(1);        }        // Вариант #1        /*        $this->socket = socket_create(AF_INET, SOCK_STREAM, SOL_TCP );        if (!socket_bind($this->socket, '0.0.0.0', $port)) {            echo "Неможливо призначити "
";            exit(1);        }        $this->listener = new EventListener($this->base,            array($this, "acceptConnCallback"), $this->base,            EventListener::OPT_CLOSE_ON_FREE | EventListener::OPT_REUSEABLE,            - 1, $this->socket);         */        // Вариант #2         $this->listener = new EventListener($this->base,             array($this, "acceptConnCallback"), $this->base,             EventListener:: OPT_CLOSE_ON_FREE | EventListener::OPT_REUSEABLE, -1,             "0.0.0.0:$port");        if (!$this->listener) {            echo "Невозможно создать слушателя";            exit(1);        }        $this->listener-> setErrorCallback(array($this, "accept_error_cb"));    }    public function dispatch() {        $this->base->dispatch();    }    // Эта функция обратного вызова будет вызвана, если в $bev есть данные для чтения    public function acceptConnCallback($listener, $fd, $address, $ctx) {        // У нас нове з'єднання! Налаштуємо bufferevent для його. *     $base==$this->base; $this->conn[] = new MyListenerConnection($base, $fd); }    public function accept_error_cb($listener, $ctx) {        $base = $this->base; fprintf(STDERR, "Помилка слухача: %d (%s). "            .".Аварійна зупинка.
",            EventUtil::getLastSocketErrno(),            EventUtil::getLastSocketError());        $base->exit(NULL);    }}$port = 9808;if ($argc > 1) {    $port = (int) $argv[ 1];}if ($port <= 0 || $port > 65535) {    exit("Некоректний порт");}$l = new MyListener($port);$l->dispatch();?> `

**Приклад #4 SSL ехо-сервер**



**Приклад #5 Обробник сигналів**

`<?php/*Запустіть в термінальному вікні:$ php examples/signal.phpУ іншому термінальному вікні знайдіть pid цього процесу і пошліть йому сигнал SIGTERM:$ ps | grep exampruslan    3976  0.2  0.0 139896 11256 pts/1    S+   10:25   0:00 php examples/signal.phpruslan    3978  0.0  0.0   9572   864 pts/2    S+   10:26   0:00 grep --color=auto examp$ kill -TERM 3976В першому вікні ви повинні побачити наступне:: Пойманий сигнал 15 * / class MyEventSignal {    private $base; function __construct($base) {         $this->base = $base; }    function eventSighandler($no, $c) {        echo "Пійман сигнал $no
";        event_base_loopexit($c->base);    }}$base = event_base_new();$c    = new MyEventSignal($base);$no   = SIGTERM;$ev   = evsignal_new($base, $no, array($c ,'eventSighandler'), $c);evsignal_add($ev);event_base_loop($base);?> `

**Приклад #6 Використання циклу libevent для обробки запитів модуля
\'eio'**

` <?php// Функція зворотного дзвінка для eio_nop()function my_nop_cb($d, $r) {    echo "step 6
";}$dir = "/tmp/abc-eio-temp";if (file_exists($dir)) {   rmdir($dir);}echo "step 1
";$base = new EventBase();echo "step 2
";eio_init();eio_mkdir($dir, 0750, EIO_PRI_DEFAULT, "my_nop_cb");$event = new Event($base, eio_get_event_stream(),|Event::$: , $base) {   echo "step 5
";   while (eio_nreqs()) {        eio_poll();    }}   $base->stop();}, $base);echo "step 
";$event->add();echo "step 4
";$base->dispatch();echo "Готово
";?> `

**Приклад #7 Різне**

`<?php/* {{{Конфігурація і підтримувані методи */echo "Підтримувані методи:
";foreach (Event::getSupportedMethods() as $m) {    echo $m, PHP_EOL;}//Уникаємо метод "select"$cfg = new EventConfig()>f| {    echo "Метод 'select' буде ігноруватися
";}//Створюємо event_base пов'язаний з конфігурацією$base = new EventBase($cfg);echo "Використовується подійний метод: ", $base->getMethod(), PHP|
";$features = $base->getFeatures();($features & EventConfig::FEATURE_ET) and print("ET - одноразове спрацьовування при перетині порога (edge-triggered IO))
");($features & EventConfig::FEATURE_O1) and print("O1 - операції додавання/видалення подій зі складністю O(1)
");($features & EventConfig::FEATURE_FDS) and print("FDS - звичайні дескриптори файлів, а не тільки сокети
");// Запрошуємо способ FDSif ($cfg->requireFeatures(EventConfig::FEATURE_FDS)) {    echo "Запитаний спосіб FDS
";   $base = new EventBase($cfg);    ($base->getFeatures() & EventConfig::FEATURE_FDS)         and print("FDS і 
");}/* }}} *//* {{{ Base */$base = new EventBase();$event = neu Event($base, STDIN, Event::READ | Event::PERSIST, function ( $fd, $events, $arg) {    static $max_iterations = 0;    if (++$max_iterations >= 5) {        /* выход после 5 итераций с паузами в 2.33 секунды */        echo "Останавливаемся...
";        $arg[0]->exit(2.33);    }   echo fgets($fd);}, array (&$base));$event->add();$base->lo Base }}} */?> `

**Приклад #8 Простий HTTP-сервер**

`<?php/* * Простий HTTP-сервер. * * Для проверки: * 1) Запускаете на любом порту, например: * $ php examples/http.php 8010 * 2) В другом терминальном окне устанавливаете к нему соединение * и делаете GET или POST запрос(другие запросы не реализованы): * $ nc -t 127.0.0.1 8010 * POST /about HTTP/1.0 * Content-Type: text/plain * Content-Length: 4 * Connection: close * ( | 1.0 200 OK * Content-Type: text/html; charset=ISO-8859-1 * Connection: close * * $ nc -t 127.0.0.1 8010 * GET/dump HTTP/1.0 * Content-Type: text/plain   натискаєте Enter) * * IПовинно вивести: * HTTP/1.0 200 OK * Content-Type: text/html; charset=ISO-8859-1 * Connection: close * (натискаєте Enter) * * $ nc -t 127.0.0.1 8010 *GET /unknown HTTP/1.0 *  -Type: text/html; charset=ISO-8859-1 * Connection: close * * 3) Дивіться, що виводиться в вікні, в якому ви запустили сервер. */function _http_dump($req, $data) {   static $counter      = 0; static $max_requests = 2; if (++$counter >= $max_requests)  {        echo "Лічильник запитів досягнув максимуму $max_requests. Виходимо
";        exit();   }}    echo __METHOD__, "метод
";   echo "запит:"; var_dump($req);    echo "дані:"; var_dump($data);   echo "
===== DUMP =====
";   echo "Команда:", $req->getCommand(), PHP_EOL;   echo "URI:", $req->getUri(), PHP_EOL;    echo " );   echo "Вихідні заголовки:"; var_dump($req->getOutputHeaders());   echo "
>> Посилаємо відповідь ...";    $req->sendReply(200, "OK");   echo "OK
";    echo "
>> Читаємо вхідний буфер ...
";|                                               
";}function _http_about($req) {    echo __METHOD__, PHP_EOL;   echo "URI: ", $req->getUri(), PHP_EOL;   ech
>> Посилаємо відповідь ...";    $req->sendReply(200, "OK");   echo "OK
";}function _http_default($req, $data) {   echo __METHOD__, PHP_EOL;    echo "URI: ", $req->getUri(), PHP_EOL;    
>> Посилаємо відповідь ...";    $req->sendReply(200, "OK");   echo "OK
";}$port = 8010;if ($argc > 1) {    $port = (int) $argv[1];}if ($port <= 0 || $port > 65535)   );}$base = new EventBase();$http = neu EventHttp($base);$http->setAllowedMethods(EventHttpRequest::CMD_GET | EventHttpRequest::CMD_POST);$http->setCallback("" _http_dump", array(4, 8));$http->setCallback("/about", __http_about");$http->setDefaultCallback("_http_default", "custom data value");$http->bind( "0.0.0.0", 8010);$base->loop();?> `

Результатом виконання цього прикладу буде щось подібне:

a=12
HTTP/1.0 200 OK
Content-Type: text/html; charset=ISO-8859-1
Connection: close

HTTP/1.0 200 OK
Content-Type: text/html; charset=ISO-8859-1
Connection: close
(тиснемо Enter)

HTTP/1.0 200 OK
Content-Type: text/html; charset=ISO-8859-1
Connection: close

**Приклад #9 Простий HTTPS-сервер**

`` <?php/* * Простий HTTPS-сервер. * * 1) Запустіть сервер: `php examples/https.php 9999` * 2) Протестуйте його: `php examples/ssl-connection.php 9999` */function _         ; static $ max_requests = 200; if (++$counter >= $max_requests)  {        echo "Лічильник запитів досягнув максимуму $max_requests. Виходимо
";        exit();   }}    echo __METHOD__, "called
";   echo "запит:"; var_dump($req);    echo "дані:"; var_dump($data);   echo "
===== DUMP =====
";   echo "Команда:", $req->getCommand(), PHP_EOL;   echo "URI:", $req->getUri(), PHP_EOL;    echo " );   echo "Вихідні заголовки:"; var_dump($req->getOutputHeaders());   echo "
>> Відправляємо відповідь ...";    $req->sendReply(200, "OK");   echo "OK
";   $buf = $req->getInputBuffer();    echo "
>> Читаємо вхідний буфер (", $buf->length, ") ...
";   while ($s = $buf->read(1024)) {       echo $s;    }    echo "
У буфері більше немає даних
";}function _http_about($req) {    echo __METHOD__, PHP_EOL;   echo "URI: ", $req->getUri(), PHP_EOL;   ech
>> Відправляємо відповідь ...";    $req->sendReply(200, "OK");   echo "OK
";}function _http_default($req, $data) {   echo __METHOD__, PHP_EOL;    echo "URI: ", $req->getUri(), PHP_EOL;    
>> Відправляємо відповідь ...";    $req->sendReply(200, "OK");   echo "OK
";}function _http_400($req) {    $req->sendError(400);}function _init_ssl() {    $local_cert = __DIR__."| k| ssl-echo-server/privkey.pem";    $ctx = new EventSslContext(EventSslContext::SSLv3_SERVER_METHOD, array (        EventSslContext::OPT_LOCAL_CERT  => $local_cert,        EventSslContext::OPT_LOCAL_PK    => $local_pk,        //EventSslContext::OPT_PASSPHRASE  => "test",      EventSslContext::OPT_ALLOW_SELF_SIGNED => true,    ));   return $ctx;}$port = 9999;if | <= 0 || $port > 65535) {   exit("Некоректний порт");}$ip = '0.0.0.0';$base = new EventBase();$ctx == _і| $base, $ctx);$http->setAllowedMethods(EventHttpRequest::CMD_GET | EventHttpRequest::CMD_POST);$http->setCallback("/dump", "_http_dump", array(4, 8));$http- >setCallback("/about", "_http_about");$http->setCallback("/err400", "_http_400");$http->setDefaultCallback("_http_default", "custom dat a value");$http->bind($ip, $port);$base->dispatch(); ``

**Приклад #10 OpenSSL з'єднання**

`<?php/* * Простий OpenSSL клієнт. * * Використання: * 1) Запускаємо сервер, наприклад так: * $ php examples/https.php 9999 * * 2) Запускаємо клента в другому окне: *  , $base) {   echo __FUNCTION__, PHP_EOL; if (is_null($req)) {         echo "Перевищений інтервал очікування
";                                            
";         } elseif ($response_code != 200) {             echo "Несподівана відповідь: $response_code
";        }}else {            echo "Сполука успішно: $response_code
";             $buf = $req->getInputBuffer();            echo "Body:
";            while ($s = $buf->readLine(EventBuffer::EOL_ANY)) {                echo $s, PHP_EOL;            }        }    }    $base->exit(NULL);}function _init_ssl() {    $ctx = new EventSslContext( EventSslContext::SSLv3_CLIENT_METHOD, array ()); <= 0 || $port > 65535) {    exit("Некоректний порт
");}$host = '127.0.0.1';$ctx = _init_ssl();if (!$ctx) {    trigger_error("Не удалося створити контекст SSL", E_USER_ER (!$base) {     trigger_error("Не удалося ініціалізувати обробник подій", E_USER_ERROR);}$conn==new EventHttpConnection($base, NULL, $host,$$; $req== new EventHttpRequest("_request_handler", $base);$req->addHeader("Host", $host, EventHttpRequest::OUTPUT_HEADER);$buf = $req->getOutputBuffer() "<html>HTML TEST</html>");//$req->addHeader("Content-Length", $buf->length, EventHttpRequest::OUTPUT_HEADER);//$req->addHeader("Connection" , "close", EventHttpRequest::OUTPUT_HEADER);$conn->makeRequest($req, EventHttpRequest::CMD_POST, "/dump");$base->dispatch();echo "END
";?> `

**Приклад #11 Приклад використання
[EventHttpConnection::makeRequest()](eventhttpconnection.makerequest.md)**

` <?phpfunction _request_handler($req, $base) {   echo __FUNCTION__, PHP_EOL; if (is_null($req)) {        echo "Timed out
";                                            
";         } elseif ($response_code != 200) {             echo "Несподівана відповідь: $response_code
";         } else {            echo "Успішне з'єднання: $response_code
";             $buf = $req->getInputBuffer();            echo "Дані:
";            while ($s = $buf->readLine(EventBuffer::EOL_ANY)) {                echo $s, PHP_EOL;            }        }    }    $base->exit(NULL);}$address = "127.0.0.1";$port = 80;$base = new EventBase();$conn = new EventHttpConnection($base, NULL, $address, $port);$conn->setTimeout(5);$req = new EventHttpRequest("_ );$req->addHeader("Host", $address, EventHttpRequest::OUTPUT_HEADER);$req->addHeader("Content-Length", "0", EventHttpRequest::OUTPUT_HEADER);$conn->ma req, EventHttpRequest::CMD_GET, "/index.cphp");$base->loop();?> `

Результатом виконання цього прикладу буде щось подібне:

_request_handler
Success: 200
Body:
PHP, date:
2013-03-13T20:27:52+05:00

**Приклад #12 Слухач з'єднань на базі сокетів UNIX**

`<?php/* * Простий echo-сервер на базі слухача з'єднань libevent. * * Використання: * 1) У першому вікні запустіть слухач: * * $ php unix-domain-listener.php [шлях к сокету] * * 2)                                                                                                     /1.sock * * 3) Почніть друком Сервер повинен повторювати введення. */class MyListenerConnection {    private $bev, $base; public function __destruct() {         if ($this->bev) {            $this->bev->free(); }    }    public function __construct($base, $fd) {       $this->base = $base; $this->bev = new EventBufferEvent($base, $fd, EventBufferEvent::OPT_CLOSE_ON_FREE); $this->bev->setCallbacks(array($this, "echoReadCallback"), NULL,            array($this, "echoEventCallback"), NULL); if (!$this->bev->enable(Event::READ)) {            echo "Не удалося дозволити читання (READ)
";            return;        }    }    public function echoReadCallback($bev, $ctx) {        // Копируем все данные из входящего буфера в исходящий буфер        $bev->output->addBuffer($bev->input);    }    public function echoEventCallback($ bev, $events, $ctx) {        if ($events & EventBufferEvent::ERROR) {            echo "Помилка в 
";        }        if ($events & (EventBufferEvent::EOF | EventBufferEvent::ERROR)) {            $bev->free();            $bev = NULL;        }    }}class MyListener {    public $base,        $listener,        $socket; private $conn = array();    public function __destruct() {        foreach ($this->conn as &$c) $c = NULL;    }    public function __construct($sock_path) {        $this->base = new EventBase() ;        if (!$this->base) {            echo "Не удаётся открыть обработчик ошибок";            exit(1);        }        if (file_exists($sock_path)) {            unlink($sock_path);        }         $this->listener = new EventListener ($this->base,             array($this, "acceptConnCallback"), $this->base,             EventListener::OPT_CLOSE_ON_FREE | EventListener::OPT_REUSEABLE, -1,             "unix:$sock_path");        if (!$this- >listener) {             trigger_error("Неможливо створити слухач", E_USER_ERROR);        }}      s, "accept_error_cb")); }    public function dispatch() {        $this->base->dispatch(); }    // Ця callback-функція буде запущена, коли в $bev з'являться дані для читання    public function acceptConnCallback($listener, $        Настроєм для нього буферевен. */         $base = $this->base; $this->conn[] = new MyListenerConnection($base, $fd); }    public function accept_error_cb($listener, $ctx) {        $base = $this->base; fprintf(STDERR, "Помилка слухача: %d (%s). "            ."Shutting down.
",            EventUtil::getLastSocketErrno(),            EventUtil::getLastSocketError());        $base->exit(NULL);    }}if ($argc <= 1) {    exit("Не указан сокет
");}$sock_path = $argv[1];$l = new MyListener($sock_path);$l->dispatch();?> `

**Приклад #13 Простий SMTP-сервер**


