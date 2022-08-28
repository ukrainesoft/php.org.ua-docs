Додати значення до обробника URL

-   [« ob\_start](function.ob-start.html)
    
-   [output\_reset\_rewrite\_vars »](function.output-reset-rewrite-vars.html)
    
-   [PHP Manual](index.html)
    
-   [Функции контроля вывода](ref.outcontrol.html)
    
-   Додати значення до обробника URL
    

# outputaddrewritevar

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

outputaddrewritevar — Додати значення до обробника URL

### Опис

```methodsynopsis
output_add_rewrite_var(string $name, string $value): bool
```

Ця функція додає ще одну пару ім'я/значення механізму перезапису URL. Ім'я та значення будуть додані до URL (як GET-параметрів) та форм (як приховані поля введення) так само, як і ідентифікатор сесії, якщо включено прозоре перезаписування посилань з використанням [session.use\_trans\_sid](session.configuration.html#ini.session.use-trans-sid)

Поведінка цієї функції контролюється параметрами php.ini [url\_rewriter.tags](outcontrol.configuration.html#ini.url-rewriter.tags) і [url\_rewriter.hosts](outcontrol.configuration.html#ini.url-rewriter.hosts)

Зауважте, що функція може бути успішно викликана не більше одного разу за запит.

> **Зауваження**: Виклик цієї функції неявно запустить буферизацію виводу, якщо вона ще не активна.

### Список параметрів

`name`

Назва параметра.

`value`

Значення параметру.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | До PHP 7.1.0 змінні перезаписи, встановлені функцією **outputaddrewritevar()**, використовують той самий буфер модуля сесії "trans sid". Починаючи з PHP 7.1.0, використовується окремий буфер, [url\_rewriter.tags](outcontrol.configuration.html#ini.url-rewriter.tags) використовується тільки для функцій виведення, доданий [url\_rewriter.hosts](outcontrol.configuration.html#ini.url-rewriter.tags) |

### Приклади

**Приклад #1 Приклад використання функції **outputaddrewritevar()****

```php
<?php
output_add_rewrite_var('var', 'value');

// несколько ссылок
echo '<a href="file.php">ссылка</a>
<a href="http://example.com">ссылка2</a>';

// форма
echo '<form action="script.php" method="post">
<input type="text" name="var2" />
</form>';

print_r(ob_list_handlers());
?>
```

Результат виконання цього прикладу:

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

-   [output\_reset\_rewrite\_vars()](function.output-reset-rewrite-vars.html) - Скинути значення обробника URL
-   [ob\_flush()](function.ob-flush.html) - Скинути (надіслати) буфер виводу
-   [ob\_list\_handlers()](function.ob-list-handlers.html) - Список всіх використовуваних обробників виводу
-   [url\_rewriter.tags](outcontrol.configuration.html#ini.url-rewriter.tags)
-   [url\_rewriter.hosts](outcontrol.configuration.html#ini.url-rewriter.hosts)
-   [session.trans\_sid\_tags](session.configuration.html#ini.session.trans-sid-tags)
-   [session.trans\_sid\_hosts](session.configuration.html#ini.session.trans-sid-hosts)