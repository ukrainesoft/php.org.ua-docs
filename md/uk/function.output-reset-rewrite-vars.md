---
navigation:
  - function.output-add-rewrite-var.md: « output\_add\_rewrite\_var
  - book.info.md: Опції/інформація PHP »
  - index.md: PHP Manual
  - ref.outcontrol.md: Функції контролю виведення
title: output\_reset\_rewrite\_vars
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# output\_reset\_rewrite\_vars

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

output\_reset\_rewrite\_vars — Скинути значення обробника URL

### Опис

```methodsynopsis
output_reset_rewrite_vars(): bool
```

Функція видаляє всі змінні перезаписи, раніше встановлені функцією [output\_add\_rewrite\_var()](function.output-add-rewrite-var.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 7.1.0 | До PHP 7.1.0, змінні перезаписи встановлені функцією [output\_add\_rewrite\_var()](function.output-add-rewrite-var.md) використовують той самий буфер модуля сесії "trans sid". З PHP 7.1.0, використовується окремий буфер і **output\_reset\_rewrite\_vars()** тільки видаляє перемінні перезаписи [output\_add\_rewrite\_var()](function.output-add-rewrite-var.md) |

### Приклади

**Приклад #1 Приклад використання функції** output\_reset\_rewrite\_vars()\*\*\*\*

```php
<?php

ini_set('url_rewriter.tags', 'a=href');

output_add_rewrite_var('var', 'value');

echo '<a href="file.php">ссылка</a>';
ob_flush();

output_reset_rewrite_vars();
echo '<a href="file.php">ссылка</a>';
?>
```

Результат виконання наведеного прикладу:

```
<a href="file.php?var=value">ссылка</a>
<a href="file.php">ссылка</a>
```

### Дивіться також

-   [output\_add\_rewrite\_var()](function.output-add-rewrite-var.md) \- Додає значення до обробника перезапису URL
-   [ob\_flush()](function.ob-flush.md) \- Скидає (відправляє) повернене активним обробником висновку значення
-   [ob\_list\_handlers()](function.ob-list-handlers.md) \- Повертає список активних обробників виводу
-   [url\_rewriter.tags](outcontrol.configuration.md#ini.url-rewriter.tags)
-   [url\_rewriter.hosts](outcontrol.configuration.md#ini.url-rewriter.hosts)
-   [session.trans\_sid\_tags](session.configuration.md#ini.session.trans-sid-tags)
-   [session.trans\_sid\_hosts](session.configuration.md#ini.session.trans-sid-hosts)
