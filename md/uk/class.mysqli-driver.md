---
navigation:
  - mysqli-result.num-rows.md: '« mysqli\_result::$num\_rows'
  - mysqli-driver.embedded-server-end.md: 'mysqli\_driver::embedded\_server\_end »'
  - index.md: PHP Manual
  - book.mysqli.md: MySQLi
title: Клас mysqli\_driver
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас mysqli\_driver

(PHP 5, PHP 7, PHP 8)

## Вступ

Класс**mysqli\_driver** є екземпляром шаблону monostate, тобто є лише один драйвер, до якого можна отримати доступ через довільну кількість екземплярів **mysqli\_driver**

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
     int
      $report_mode;

   }
```

## Властивості

client\_info

Версія заголовка Client API

client\_version

Версія Client

driver\_version

Версія MySQLi Driver

**Увага**

Властивість оголошено *застарілим*в PHP 8.1.0. Полагаться на свойство крайне не рекомендуется.

embedded

Статус підтримки MySQLi Embedded

**Увага**

Свойство*видалено* у PHP 8.0.0.

reconnect

Дозволити або заборонити перепідключення (дивіться INI-директиву [mysqli.reconnect](mysqli.configuration.md#ini.mysqli.reconnect)) .

**Увага**

Властивість була *видалено* разом із INI-директивою [mysqli.reconnect](mysqli.configuration.md#ini.mysqli.reconnect) у PHP 8.2.0.

report\_mode

Установить\*\*`MYSQLI_REPORT_OFF`\*\* **`MYSQLI_REPORT_ALL`** або будь-яку комбінацію з **`MYSQLI_REPORT_STRICT`** (виклик винятків для помилок), **`MYSQLI_REPORT_ERROR`** (повідомлення про помилки) та **`MYSQLI_REPORT_INDEX`** (Помилки, пов'язані з індексами). Дивіться також [mysqli\_report()](function.mysqli-report.md)

## список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Властивість mysqli\_driver::$reconnect було видалено. |
| 8.1.0 | Властивість mysqli\_driver::$driver\_version оголошено застарілим. |
| 8.0.0 | Властивість mysqli\_driver::$embedded було видалено. |
| 7.4.0 | Метод[mysqli\_driver::embedded\_server\_start()](mysqli-driver.embedded-server-start.md)и**mysqli\_driver:embedded\_server\_end()** були вилучені. |

## Зміст

-   [mysqli\_driver::embedded\_server\_end](mysqli-driver.embedded-server-end.md) \- Зупиняє вбудований сервер
-   [mysqli\_driver::embedded\_server\_start](mysqli-driver.embedded-server-start.md)— Ініціалізує та запускає вбудований сервер
-   [mysqli\_driver::$report\_mode](mysqli-driver.report-mode.md)— Встановлює режим звіту про помилки mysqli
