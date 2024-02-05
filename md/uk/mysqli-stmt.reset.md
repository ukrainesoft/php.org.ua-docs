---
navigation:
  - mysqli-stmt.prepare.md: '« mysqli\_stmt::prepare'
  - mysqli-stmt.result-metadata.md: 'mysqli\_stmt::result\_metadata »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqli\_stmt
title: 'mysqli\_stmt::reset'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_stmt::reset

# mysqli\_stmt\_reset

(PHP 5, PHP 7, PHP 8)

mysqli\_stmt::reset -- mysqli\_stmt\_reset — Скидає результати підготовленого запиту.

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

Скидає запит на сервер, а також дані, передані на сервер функцією [mysqli\_stmt\_send\_long\_data()](mysqli-stmt.send-long-data.md), очищає буфер результатів запиту та поточні помилки. Функція не видаляє прив'язки параметрів запиту, а також надані на клієнта результуючі набори. Результуючі набори, що містяться на клієнті, будуть очищені при наступному виконанні запиту (або його закритті).

Для подготовки запроса с другим SQL-текстом, используйте функцию[mysqli\_stmt\_prepare()](mysqli-stmt.prepare.md)

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.md), який повернула функція [mysqli\_stmt\_init()](mysqli.stmt-init.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [mysqli\_prepare()](mysqli.prepare.md) \- готує SQL вираз до виконання
