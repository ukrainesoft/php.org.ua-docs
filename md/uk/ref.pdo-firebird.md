---
navigation:
  - ref.pdo-dblib.connection.md: « PDO\_DBLIB DSN
  - ref.pdo-firebird.connection.md: PDO\_FIREBIRD DSN »
  - index.md: PHP Manual
  - pdo.drivers.md: Драйвери PDO
title: Функції Firebird (PDO\_FIREBIRD)
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Функції Firebird (PDO\_FIREBIRD)

## Вступ

PDO\_FIREBIRD – драйвер, що реалізує інтерфейс PHP Data Objects (PDO) для доступу до баз даних Firebird.

## Установка

Для установки модуля PDO Firebird используйте опцию**\--with-pdo-firebird\[=DIR\]**, где`[=DIR]` вказує на директорію установки Firebird.

```
$ ./configure --with-pdo-firebird
```

## Обумовлені константи

Наведені нижче константи визначені цим драйвером і будуть доступні лише у випадку, якщо PHP був зібраний за допомогою цього модуля, або модуль був динамічно завантажений під час виконання. Крім того, ці залежні від драйвера константи повинні бути використані лише разом із цим драйвером. Використання атрибутів, специфічних для деякого драйвера з іншим драйвером, може викликати несподівану поведінку. Якщо ваш код виконується з кількома драйверами, можна використовувати функцію [PDO::getAttribute()](pdo.getattribute.md)для получения атрибута\*\*`PDO::ATTR_DRIVER_NAME`\*\*для проверки драйвера.

**`PDO::FB_ATTR_DATE_FORMAT`**(int)

встановлює формат дати.

**`PDO::FB_ATTR_TIME_FORMAT`**(int)

Встановлює формат часу.

**`PDO::FB_ATTR_TIMESTAMP_FORMAT`**(int)

Встановлює формат тимчасової позначки.

## Зміст

-   [PDO\_FIREBIRD DSN](ref.pdo-firebird.connection.md) \- З'єднання з базою Firebird
