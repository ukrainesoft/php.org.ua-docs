---
navigation:
  - mysqli-result.num-rows.md: '« mysqliresult::$numrows'
  - mysqli-driver.embedded-server-end.md: 'mysqlidriver::embeddedserverend »'
  - index.md: PHP Manual
  - book.mysqli.md: MySQLi
title: Клас mysqlidriver
---
# Клас mysqlidriver

(PHP 5, PHP 7, PHP 8)

## Вступ

Клас **mysqlidriver** є екземпляром шаблону monostate, тобто є лише один драйвер, до якого можна отримати доступ через довільну кількість екземплярів **mysqlidriver**

## Огляд класів

```classsynopsis

     
    

    
     
      final
      class mysqli_driver
     
     {

    /* Свойства */
    
     public
     readonly
     string
      $client_info;

    public
     readonly
     int
      $client_version;

    public
     readonly
     int
      $driver_version;

    public
     readonly
     bool
      $embedded;

    public
     bool
      $reconnect = false;

    public
     int
      $report_mode;


    /* Методы */
    
   public embedded_server_end(): void
public embedded_server_start(int $start, array $arguments, array $groups): bool

   }
```

## Властивості

clientinfo

Версія заголовка Client API

clientversion

Версія Client

driverversion

Версія MySQLi Driver

**Увага**

Властивість оголошено *застарілим* у PHP 8.1.0. Покладатися на властивість не рекомендується.

embedded

Статус підтримки MySQLi Embedded

**Увага**

Властивість *видалено* у PHP 8.0.0.

reconnect

Дозволити або заборонити перепідключення (дивіться INI-директиву mysqli.reconnect)

reportmode

Встановити **`MYSQLI_REPORT_OFF`** **`MYSQLI_REPORT_ALL`** або будь-яку комбінацію з **`MYSQLI_REPORT_STRICT`** (виклик винятків для помилок), **`MYSQLI_REPORT_ERROR`** (повідомлення про помилки) та **`MYSQLI_REPORT_INDEX`** (Помилки, пов'язані з індексами). Дивіться також [mysqlireport()](function.mysqli-report.md)

## Зміст

-   [mysqlidriver::embeddedserverend](mysqli-driver.embedded-server-end.md) - Зупиняє вбудований сервер
-   [mysqlidriver::embeddedserverstart](mysqli-driver.embedded-server-start.md) — Ініціалізує та запускає вбудований сервер
-   [mysqlidriver::$reportmode](mysqli-driver.report-mode.md) — Встановлює режим звіту про помилки mysqli
