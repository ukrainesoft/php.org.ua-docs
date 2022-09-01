---
navigation:
  - ref.pdo-dblib.connection.html: « PDODBLIB DSN
  - ref.pdo-firebird.connection.html: PDOFIREBIRD DSN »
  - index.html: PHP Manual
  - pdo.drivers.html: Драйвери PDO
title: Функції Firebird (PDOFIREBIRD)
---
# Функції Firebird (PDOFIREBIRD)

## Вступ

PDOFIREBIRD – драйвер, що реалізує інтерфейс PHP Data Objects (PDO) для доступу до баз даних Firebird.

## Встановлення

Для встановлення модуля PDO Firebird використовуйте опцію **\-with-pdo-firebird=DIR**, де `[=DIR]` вказує на директорію установки Firebird.

```
$ ./configure --with-pdo-firebird
```

## Обумовлені константи

Наведені нижче константи визначені цим драйвером і будуть доступні лише у випадку, якщо PHP був зібраний з підтримкою цього модуля, або цей модуль був динамічно завантажений під час виконання. Крім того, ці залежні від драйвера константи повинні бути використані лише разом із цим драйвером. Використання атрибутів, специфічних для деякого драйвера з іншим драйвером, може викликати несподівану поведінку. Якщо ваш код виконується з кількома драйверами, можна використовувати функцію [PDO::getAttribute()](pdo.getattribute.md) для отримання атрибуту **`PDO::ATTR_DRIVER_NAME`** для перевірки драйвера.

**`PDO::FB_ATTR_DATE_FORMAT`** (int)

встановлює формат дати.

**`PDO::FB_ATTR_TIME_FORMAT`** (int)

Встановлює формат часу.

**`PDO::FB_ATTR_TIMESTAMP_FORMAT`** (int)

Встановлює формат тимчасової позначки.

## Зміст

-   [PDOFIREBIRD DSN](ref.pdo-firebird.connection.md) - З'єднання з базою Firebird
