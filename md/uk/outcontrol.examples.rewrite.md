Використання перезапису виводу

-   [« Базовое использование](outcontrol.examples.basic.html)
    
-   [Функції контролю виведення](ref.outcontrol.html)
    
-   [PHP Manual](index.html)
    
-   [Приклади](outcontrol.examples.html)
    
-   Використання перезапису виводу
    

## Використання перезапису виводу

Починаючи з PHP 7.1.0, [outputaddrewritevar()](function.output-add-rewrite-var.html) і [outputresetrewritevars()](function.output-reset-rewrite-vars.html) використовують окремий буфер виводу, тобто не використовують буфер виводу [прозорої підтримки sid](session.configuration.html#ini.session.use-trans-sid)

**Приклад #1 Приклад перезапису виводу**

```php
<?php
// Этот код работает с PHP 7.1.0, 7.0.10, 5.6.25 и выше.

// HTTP_HOST - целевой хост по умолчанию. Зададим сами, чтобы код примера заработал.
$_SERVER['HTTP_HOST'] = 'php.net';

// Перезаписыватель вывода перезаписывает только "form". Добавим a=href.
// Теги должны указываться как tag_name=url_attr, то есть img=src,iframe=src
// Между настройками пробелы недопустимы.
// Тег "form" - специальный тег, в который добавляется скрытый "input"
ini_set('url_rewriter.tags','a=href,form=');
var_dump(ini_get('url_rewriter.tags'));

// Это добавлено в URL и "form"
output_add_rewrite_var('test', 'value');
?>
<a href="//php.net/index.php?bug=1234">bug1234</a>
<form action="https://php.net/?bug=1234&edit=1" action="post">
 <input type="text" name="title" />
</form>
```

Результат виконання цього прикладу:

```
<a href="//php.net/?bug=1234&test=value">bug1234</a>
<form action="https://php.net/?bug=1234&edit=1" method="post"><input type="hidden" name="test" value="value" />
 <input type="text" name="title" />
</form>
```

З PHP 7.1.0, функції перезапису виводу мають власні INI-настройки . [urlrewriter.tags](outcontrol.configuration.html#ini.url-rewriter.tags) і [urlrewriter.hosts](outcontrol.configuration.html#ini.url-rewriter.hosts)