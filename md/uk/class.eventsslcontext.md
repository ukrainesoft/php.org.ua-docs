---
navigation:
  - eventlistener.seterrorcallback.md: '« EventListener::setErrorCallback'
  - eventsslcontext.construct.md: 'EventSslContext::\_\_construct »'
  - index.md: PHP Manual
  - book.event.md: Event
title: Клас EventSslContext
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас EventSslContext

(PECL event >= 1.2.6-beta)

## Вступ

Представляет структуру`SSL_CTX`. Надає методи та властивості для налаштування контексту SSL.

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

local\_cert

Шлях до локального файлу сертифіката. Це має бути файл у форматі PEM, який містить сертифікат. Опціонально може містити ланцюжок сертифікатів емітентів.

local\_pk

Шлях до локального файлу з приватним ключем

## Обумовлені константи

**`EventSslContext::SSLv2_CLIENT_METHOD`**

Метод клиента SSLv2. Смотрите руководство по`SSL_CTX_new(3)`

**`EventSslContext::SSLv3_CLIENT_METHOD`**

Метод клиента SSLv3. Смотрите руководство по`SSL_CTX_new(3)`

**`EventSslContext::SSLv23_CLIENT_METHOD`**

Метод клиента SSLv23. Смотрите руководство по`SSL_CTX_new(3)`

**`EventSslContext::TLS_CLIENT_METHOD`**

Метод клиента TLS. Смотрите руководство по`SSL_CTX_new(3)`

**`EventSslContext::SSLv2_SERVER_METHOD`**

Метод сервера SSLv2. Смотрите руководство по`SSL_CTX_new(3)`

**`EventSslContext::SSLv3_SERVER_METHOD`**

Метод сервера SSLv3. Смотрите руководство по`SSL_CTX_new(3)`

**`EventSslContext::SSLv23_SERVER_METHOD`**

Метод сервера SSLv23. Смотрите руководство по`SSL_CTX_new(3)`

**`EventSslContext::TLS_SERVER_METHOD`**

Метод сервера TLS. Смотрите руководство по`SSL_CTX_new(3)`

**`EventSslContext::OPT_LOCAL_CERT`**

Ключ елемента в масиві опцій, переданому в [EventSslContext::\_\_construct()](eventsslcontext.construct.md) . Опція вказує шлях локального сертифіката.

**`EventSslContext::OPT_LOCAL_PK`**

Ключ елемента в масиві опцій, переданому в [EventSslContext::\_\_construct()](eventsslcontext.construct.md) . Опція вказує на шлях локального приватного ключа.

**`EventSslContext::OPT_PASSPHRASE`**

Ключ елемента в масиві опцій, переданому в [EventSslContext::\_\_construct()](eventsslcontext.construct.md). Представляет пароль сертификата.

**`EventSslContext::OPT_CA_FILE`**

Ключ елемента в масиві опцій, переданому в [EventSslContext::\_\_construct()](eventsslcontext.construct.md). Представляет путь к файлу центра сертификации.

**`EventSslContext::OPT_CA_PATH`**

Ключ елемента в масиві опцій, переданому в [EventSslContext::\_\_construct()](eventsslcontext.construct.md) . Представляє шлях, яким потрібно шукати файл центру сертифікації.

**`EventSslContext::OPT_ALLOW_SELF_SIGNED`**

Ключ елемента в масиві опцій, переданому в [EventSslContext::\_\_construct()](eventsslcontext.construct.md) . Надає опцію, що дозволяє використовувати самопідписані сертифікати.

**`EventSslContext::OPT_VERIFY_PEER`**

Ключ елемента в масиві опцій, переданому в [EventSslContext::\_\_construct()](eventsslcontext.construct.md) . Надає опцію, що вказує модулю Event перевіряти вузли.

**`EventSslContext::OPT_VERIFY_DEPTH`**

Ключ елемента в масиві опцій, переданому в [EventSslContext::\_\_construct()](eventsslcontext.construct.md). Представляет максимальную глубину проверки цепочки сертификатов, допустимую для контекста SSL.

**`EventSslContext::OPT_CIPHERS`**

Ключ елемента в масиві опцій, переданому в [EventSslContext::\_\_construct()](eventsslcontext.construct.md). Представляет список шифров для контекста SSL.

## Зміст

-   [EventSslContext::\_\_construct](eventsslcontext.construct.md)— Створює контекст OpenSSL для класів модуля Event
