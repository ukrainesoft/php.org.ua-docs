---
navigation:
  - function.output-add-rewrite-var.md: « outputaddrewritevar
  - book.info.md: Опции/информация PHP »
  - index.md: PHP Manual
  - ref.outcontrol.md: Функції контролю виведення
title: outputresetrewritevars
---
# outputresetrewritevars

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

outputresetrewritevars — Скинути значення обробника URL

### Опис

```methodsynopsis
output_reset_rewrite_vars(): bool
```

Ця функція скидає обробник URL та видаляє всі значення, встановлені функцією [outputaddrewritevar()](function.output-add-rewrite-var.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | До PHP 7.1.0, змінні перезаписи встановлені функцією [outputaddrewritevar()](function.output-add-rewrite-var.md) використовують той самий буфер модуля сесії "trans sid". З PHP 7.1.0, використовується окремий буфер і **outputresetrewritevars()** тільки видаляє перемінні перезаписи [outputaddrewritevar()](function.output-add-rewrite-var.md) |

### Приклади

**Приклад #1 Приклад використання функції **outputresetrewritevars()****

```php
<?php
session_start();
output_add_rewrite_var('var', 'value');

echo '<a href="file.php">ссылка</a>';
ob_flush();

output_reset_rewrite_vars();
echo '<a href="file.php">ссылка</a>';
?>
```

Результат виконання цього прикладу:

```
<a href="file.php?PHPSESSID=xxx&var=value">ссылка</a>
<a href="file.php">ссылка</a>
```

### Дивіться також

-   [outputaddrewritevar()](function.output-add-rewrite-var.md) - Додати значення в обробник URL
-   [проflush()](function.ob-flush.md) - Скинути (надіслати) буфер виводу
-   [проlisthandlers()](function.ob-list-handlers.md) - Список всіх використовуваних обробників виводу
-   [urlrewriter.tags](outcontrol.configuration.md#ini.url-rewriter.tags)
-   [urlrewriter.hosts](outcontrol.configuration.md#ini.url-rewriter.hosts)
-   [session.transsidtags](session.configuration.md#ini.session.trans-sid-tags)
-   [session.transsidhosts](session.configuration.md#ini.session.trans-sid-hosts)
