---
navigation:
  - varnish.example.log.md: « Просте використання VarnishLog
  - varnishadmin.auth.md: 'VarnishAdmin::auth »'
  - index.md: PHP Manual
  - book.varnish.md: Varnish
title: Клас VarnishAdmin
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас VarnishAdmin

(PECL varnish >= 0.3)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class VarnishAdmin
     
     {


    /* Методы */
    
   public auth(): bool
public ban(string $vcl_regex): int
public banUrl(string $vcl_regex): int
public clearPanic(): int
public connect(): bool
public __construct(array $args = ?)
public disconnect(): bool
public getPanic(): string
public getParams(): array
public isRunning(): bool
public setCompat(int $compat): void
public setHost(string $host): void
public setIdent(string $ident): void
public setParam(string $name, string|int $value): int
public setPort(int $port): void
public setSecret(string $secret): void
public setTimeout(int $timeout): void
public start(): int
public stop(): int

   }
```

## Зміст

-   [VarnishAdmin::auth](varnishadmin.auth.md)— Аутентифікація на екземплярі varnish
-   [VarnishAdmin::ban](varnishadmin.ban.md)— Заборонити URL-адресу за допомогою виразу VCL
-   [VarnishAdmin::banUrl](varnishadmin.banurl.md)— Заборонити URL-адресу, використовуючи вираз VCL
-   [VarnishAdmin::clearPanic](varnishadmin.clearpanic.md)— Очистити критичні повідомлення екземпляра varnish
-   [VarnishAdmin::connect](varnishadmin.connect.md)— Підключення до інтерфейсу адміністрування екземпляра varnish
-   [VarnishAdmin::\_\_construct](varnishadmin.construct.md)— VarnishAdmin constructor
-   [VarnishAdmin::disconnect](varnishadmin.disconnect.md)— Відключення від інтерфейсу адміністрування екземпляра varnish
-   [VarnishAdmin::getPanic](varnishadmin.getpanic.md)— Отримати останнє критичне повідомлення на екземплярі varnish
-   [VarnishAdmin::getParams](varnishadmin.getparams.md)— Отримати параметри конфігурації поточного екземпляра varnish
-   [VarnishAdmin::isRunning](varnishadmin.isrunning.md)— Перевірити, чи виконується зараз підпорядкований процес varnish
-   [VarnishAdmin::setCompat](varnishadmin.setcompat.md)— Встановити параметр конфігурації класу compat
-   [VarnishAdmin::setHost](varnishadmin.sethost.md)— Встановити параметр конфігурації host класу
-   [VarnishAdmin::setIdent](varnishadmin.setident.md)— Встановити параметр конфігурації ident класу
-   [VarnishAdmin::setParam](varnishadmin.setparam.md)— Встановити параметр конфігурації на поточному екземплярі varnish
-   [VarnishAdmin::setPort](varnishadmin.setport.md)— Встановити параметр конфігурації класу port
-   [VarnishAdmin::setSecret](varnishadmin.setsecret.md)— Встановити параметр конфігурації secret класу
-   [VarnishAdmin::setTimeout](varnishadmin.settimeout.md)— Встановити параметр конфігурації timeout класу
-   [VarnishAdmin::start](varnishadmin.start.md)— Запустити робочий процес varnish
-   [VarnishAdmin::stop](varnishadmin.stop.md)— Зупинити робочий процес varnish
