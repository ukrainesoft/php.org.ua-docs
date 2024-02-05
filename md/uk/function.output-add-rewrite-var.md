---
navigation:
  - function.ob-start.md: « ob\_start
  - function.output-reset-rewrite-vars.md: output\_reset\_rewrite\_vars »
  - index.md: PHP Manual
  - ref.outcontrol.md: Функції контролю виведення
title: output\_add\_rewrite\_var
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# output\_add\_rewrite\_var

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

output\_add\_rewrite\_var — Додає значення до обробника перезапису URL

### Опис

```methodsynopsis
output_add_rewrite_var(string $name, string $value): bool
```

Функція запускає обробник буфера виводу `«URL-Rewriter»`якщо він не активний, зберігає значення параметрів `name`и`value`, і коли буфер скидається, перезаписує URL-адреси та форми на основі придатних ini-налаштувань. Чергові дзвінки функції зберігатимуть усі додаткові пари ім'я/значення доти, доки обробник не буде вимкнений.

Коли буфер виведення скидається (викликом функцій [ob\_flush()](function.ob-flush.md) [ob\_end\_flush()](function.ob-end-flush.md) [ob\_get\_flush()](function.ob-get-flush.md) або наприкінці роботи скрипта), обробник `«URL-Rewriter»` додає в атрибути HTML-тегів пари ім'я/значення як параметри запиту для URL-адрес та приховані поля на основі значень директив конфігурації [url\_rewriter.tags](outcontrol.configuration.md#ini.url-rewriter.tags) і [url\_rewriter.hosts](outcontrol.configuration.md#ini.url-rewriter.hosts) у форми.

Каждая пара имя/значение, добавленная в обработчик`«URL-Rewriter»`, буде додано до URL-адреси та/або форми, навіть якщо це призведе до дублювання URL-параметрів запиту або елементів із однаковими назвами атрибутів.

> **Зауваження**: После отключения обработчика`«URL-Rewriter»` його неможливо запустити знову.

### Список параметрів

`name`

Назва параметра.

`value`

Значення параметра.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 7.1.0 | Починаючи з PHP 7.1.0, функція використовує виділений буфер виводу, директива [url\_rewriter.tags](outcontrol.configuration.md#ini.url-rewriter.tags) враховується лише під час роботи з функціями виведення, а директива [url\_rewriter.hosts](outcontrol.configuration.md#ini.url-rewriter.tags) доступна. До PHP 7.1.0 змінні перезаписи, встановлені функціями **output\_add\_rewrite\_var()**, використовували загальний буфер виводу за допомогою прозорого ідентифікатора сесії (див. опис директиви [session.trans\_sid\_tags](session.configuration.md#ini.session.trans-sid-tags) |

### Приклади

**Приклад #1 Приклад использования функции**output\_add\_rewrite\_var()\*\*\*\*

```php
<?php

ini_set('url_rewriter.tags', 'a=href,form=');

output_add_rewrite_var('var', 'value');

// несколько ссылок
echo '<a href="file.php">ссылка</a>
<a href="http://example.com">ссылка2</a>';

// форма
echo '<form action="script.php" method="post">
<input type="text" name="var2" />
</form>';

print_r(ob_list_handlers());
?>
```

Результат виконання наведеного прикладу:

```
<a href="file.php?var=value">ссылка</a>
<a href="http://example.com">ссылка2</a>

<form action="script.php" method="post">
<input type="hidden" name="var" value="value" />
<input type="text" name="var2" />
</form>

Array
(
    [0] => URL-Rewriter
)
```

### Дивіться також

-   [output\_reset\_rewrite\_vars()](function.output-reset-rewrite-vars.md) \- Скинути значення обробника URL
-   [ob\_flush()](function.ob-flush.md) \- Скидає (відправляє) повернене активним обробником висновку значення
-   [ob\_list\_handlers()](function.ob-list-handlers.md) \- Повертає список активних обробників виводу
-   [url\_rewriter.tags](outcontrol.configuration.md#ini.url-rewriter.tags)
-   [url\_rewriter.hosts](outcontrol.configuration.md#ini.url-rewriter.hosts)
