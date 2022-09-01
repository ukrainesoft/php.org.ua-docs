---
navigation:
  - mysqli-stmt.prepare.html: '« mysqlistmt::prepare'
  - mysqli-stmt.result-metadata.html: 'mysqlistmt::resultmetadata »'
  - index.html: PHP Manual
  - class.mysqli-stmt.html: mysqlistmt
title: 'mysqlistmt::reset'
---
# mysqlistmt::reset

# mysqlistmtreset

(PHP 5, PHP 7, PHP 8)

mysqlistmt::reset -- mysqlistmtreset — Скидає результати підготовленого запиту.

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::reset(): bool
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_reset(mysqli_stmt $statement): bool
```

Скидає результати виконання підготовленого запиту на клієнта та на сервері та переводить запит у стан, як після підготовки.

Скидає запит на сервері, а також дані, передані на сервер функцією [mysqlistmtsendlongdata()](mysqli-stmt.send-long-data.md), очищає буфер результатів запиту та поточні помилки. Функція не видаляє прив'язки параметрів запиту, а також надані на клієнта результуючі набори. Результуючі набори, що містяться на клієнті, будуть очищені при наступному виконанні запиту (або його закритті).

Для підготовки запиту з іншим текстом SQL, використовуйте функцію [mysqlistmtprepare()](mysqli-stmt.prepare.md)

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqlistmt](class.mysqli-stmt.html), отриманий за допомогою [mysqlistmtinit()](mysqli.stmt-init.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [mysqliprepare()](mysqli.prepare.md) - готує SQL вираз до виконання
