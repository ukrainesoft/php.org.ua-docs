Клас EventSslContext

-   [« EventListener::setErrorCallback](eventlistener.seterrorcallback.html)
    
-   [EventSslContext::\_\_construct »](eventsslcontext.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Event](book.event.html)
    
-   Клас EventSslContext
    

# Клас EventSslContext

(PECL event >= 1.2.6-beta)

## Вступ

Представляє структуру `SSL_CTX`. Надає методи та властивості для налаштування контексту SSL.

## Огляд класів

```classsynopsis

     
    
    
    
     
      final
      class EventSslContext
     
     {
    
    /* Константы */
    
     const
     int
      SSLv2_CLIENT_METHOD = 1;

    const
     int
      SSLv3_CLIENT_METHOD = 2;

    const
     int
      SSLv23_CLIENT_METHOD = 3;

    const
     int
      TLS_CLIENT_METHOD = 4;

    const
     int
      SSLv2_SERVER_METHOD = 5;

    const
     int
      SSLv3_SERVER_METHOD = 6;

    const
     int
      SSLv23_SERVER_METHOD = 7;

    const
     int
      TLS_SERVER_METHOD = 8;

    const
     int
      OPT_LOCAL_CERT = 1;

    const
     int
      OPT_LOCAL_PK = 2;

    const
     int
      OPT_PASSPHRASE = 3;

    const
     int
      OPT_CA_FILE = 4;

    const
     int
      OPT_CA_PATH = 5;

    const
     int
      OPT_ALLOW_SELF_SIGNED = 6;

    const
     int
      OPT_VERIFY_PEER = 7;

    const
     int
      OPT_VERIFY_DEPTH = 8;

    const
     int
      OPT_CIPHERS = 9;

    /* Свойства */
    public
     string
      $local_cert;

    public
     string
      $local_pk;

    /* Методы */
    
   public
   __construct(
    string
     $method
   , 
    string
     $options
   )

   }
```

## Властивості

localcert

Шлях до локального файлу сертифіката. Це має бути файл у форматі PEM, який містить сертифікат. Опціонально може містити ланцюжок сертифікатів емітентів.

localпк

Шлях до локального файлу з приватним ключем

## Обумовлені константи

**`EventSslContext::SSLv2_CLIENT_METHOD`**

Метод клієнта SSLv2. Дивіться посібник з `SSL_CTX_new(3)`

**`EventSslContext::SSLv3_CLIENT_METHOD`**

Метод клієнта SSLv3. Дивіться посібник з `SSL_CTX_new(3)`

**`EventSslContext::SSLv23_CLIENT_METHOD`**

Метод клієнта SSLv23. Дивіться посібник з `SSL_CTX_new(3)`

**`EventSslContext::TLS_CLIENT_METHOD`**

Спосіб клієнта TLS. Дивіться посібник з `SSL_CTX_new(3)`

**`EventSslContext::SSLv2_SERVER_METHOD`**

Метод сервера SSLv2. Дивіться посібник з `SSL_CTX_new(3)`

**`EventSslContext::SSLv3_SERVER_METHOD`**

Метод сервера SSLv3. Дивіться посібник з `SSL_CTX_new(3)`

**`EventSslContext::SSLv23_SERVER_METHOD`**

Метод сервера SSLv23. Дивіться посібник з `SSL_CTX_new(3)`

**`EventSslContext::TLS_SERVER_METHOD`**

Метод сервера TLS. Дивіться посібник з `SSL_CTX_new(3)`

**`EventSslContext::OPT_LOCAL_CERT`**

Ключ елемента в масиві опцій, переданому в [EventSslContext::\_\_construct()](eventsslcontext.construct.html) . Опція вказує шлях локального сертифіката.

**`EventSslContext::OPT_LOCAL_PK`**

Ключ елемента в масиві опцій, переданому в [EventSslContext::\_\_construct()](eventsslcontext.construct.html) . Опція вказує на шлях локального приватного ключа.

**`EventSslContext::OPT_PASSPHRASE`**

Ключ елемента в масиві опцій, переданому в [EventSslContext::\_\_construct()](eventsslcontext.construct.html) . Надає пароль сертифіката.

**`EventSslContext::OPT_CA_FILE`**

Ключ елемента в масиві опцій, переданому в [EventSslContext::\_\_construct()](eventsslcontext.construct.html) . Це шлях до файлу центру сертифікації.

**`EventSslContext::OPT_CA_PATH`**

Ключ елемента в масиві опцій, переданому в [EventSslContext::\_\_construct()](eventsslcontext.construct.html) . Представляє шлях, яким потрібно шукати файл центру сертифікації.

**`EventSslContext::OPT_ALLOW_SELF_SIGNED`**

Ключ елемента в масиві опцій, переданому в [EventSslContext::\_\_construct()](eventsslcontext.construct.html) . Надає опцію, що дозволяє використовувати самопідписані сертифікати.

**`EventSslContext::OPT_VERIFY_PEER`**

Ключ елемента в масиві опцій, переданому в [EventSslContext::\_\_construct()](eventsslcontext.construct.html) . Надає опцію, що вказує модулю Event перевіряти вузли.

**`EventSslContext::OPT_VERIFY_DEPTH`**

Ключ елемента в масиві опцій, переданому в [EventSslContext::\_\_construct()](eventsslcontext.construct.html) . Представляє максимальну глибину перевірки ланцюжка сертифікатів, допустиму для контексту SSL.

**`EventSslContext::OPT_CIPHERS`**

Ключ елемента в масиві опцій, переданому в [EventSslContext::\_\_construct()](eventsslcontext.construct.html) . Надає список шифрів для контексту SSL.

## Зміст

-   [EventSslContext::\_\_construct](eventsslcontext.construct.html) — Конструктор контексту OpenSSL для використання у класах Event