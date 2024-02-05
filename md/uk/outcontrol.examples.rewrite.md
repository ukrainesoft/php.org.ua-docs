---
navigation:
  - outcontrol.examples.basic.md: « Основи
  - ref.outcontrol.md: Функції контролю виведення
  - index.md: PHP Manual
  - outcontrol.examples.md: Приклади
title: Перезапис виводу
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Перезапис виводу

Починаючи з PHP 7.1.0 функції [output\_add\_rewrite\_var()](function.output-add-rewrite-var.md) і [output\_reset\_rewrite\_vars()](function.output-reset-rewrite-vars.md) працюють із окремим буфером виведення, тобто не працюють із буфером виведення [прозорої підтримки sid](session.configuration.md#ini.session.use-trans-sid)

**Приклад #1 Приклад перезапису виводу**

```php
<?php

// Этот код работает с PHP 7.1.0, 7.0.10, 5.6.25 и выше.

// HTTP_HOST — целевой хост по умолчанию. Зададим, чтобы код примера заработал.
$_SERVER['HTTP_HOST'] = 'php.net';

// Обработчик перезаписи вывода перезаписывает только «form». Добавим a=href.
// Теги должны быть указаны как tag_name=url_attr, то есть img=src,iframe=src
// Пробелы между настройками не разрешены.
// Тег «form» — тег, который добавляет скрытые поля «input»
ini_set('url_rewriter.tags','a=href,form=');
var_dump(ini_get('url_rewriter.tags'));

// Это будет добавлено в URL и «form»
output_add_rewrite_var('test', 'value');
?>
<a href="//php.net/index.php?bug=1234">bug1234</a>
<form action="https://php.net/?bug=1234&edit=1" method="post">
 <input type="text" name="title" />
</form>
```

Результат виконання наведеного прикладу:

```
<a href="//php.net/?bug=1234&test=value">bug1234</a>
<form action="https://php.net/?bug=1234&edit=1" method="post"><input type="hidden" name="test" value="value" />
 <input type="text" name="title" />
</form>
```

З PHP 7.1.0 у функцій перезапису виводу з'явилися окремі INI-налаштування. [url\_rewriter.tags](outcontrol.configuration.md#ini.url-rewriter.tags) і [url\_rewriter.hosts](outcontrol.configuration.md#ini.url-rewriter.hosts)
