Зміна завантажувача за умовчанням для зовнішніх об'єктів

-   [« libxmlgetlasterror](function.libxml-get-last-error.html)
    
-   [libxmlsetstreamscontext »](function.libxml-set-streams-context.html)
    
-   [PHP Manual](index.html)
    
-   [Функції libxml](ref.libxml.html)
    
-   Зміна завантажувача за умовчанням для зовнішніх об'єктів
    

# libxmlsetexternalentityloader

(PHP 5> = 5.4.0, PHP 7, PHP 8)

libxmlsetexternalentityloader — Змінити завантажувач за умовчанням для зовнішніх об'єктів

### Опис

```methodsynopsis
libxml_set_external_entity_loader(?callable $resolver_function): bool
```

Зміна стандартного завантажувача для зовнішніх об'єктів. Можна використовувати для придушення розширення довільних зовнішніх сутностей, щоб уникнути XXE-атак, навіть якщо для відповідної операції встановлено значення **`LIBXML_NOENT`**. Зазвичай це краще, ніж виклик [libxmldisableentityloader()](function.libxml-disable-entity-loader.html)

### Список параметрів

`resolver_function`

Callback-функція ([callable](language.types.callable.html)) з наступною сигнатурою:

```methodsynopsis
resolver(string $public_id, string $system_id, array $context): resource|string|null
```

`public_id`

Громадський ідентифікатор.

`system_id`

Системний ідентифікатор.

`context`

Масив із чотирьох елементів: `"directory"` `"intSubName"` `"extSubURI"` і `"extSubSystem"`

Ця callback-функція повинна повертати ресурс ([resource](language.types.resource.html)) або рядок (string) з якого можна відкрити ресурс. Якщо повертається **`null`**, роздільна здатність посилання на сутність завершиться помилкою.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **libxmlsetexternalentityloader()****

```php
<?php
$xml = <<<XML
<!DOCTYPE foo PUBLIC "-//FOO/BAR" "http://example.com/foobar">
<foo>bar</foo>
XML;

$dtd = <<<DTD
<!ELEMENT foo (#PCDATA)>
DTD;

libxml_set_external_entity_loader(
    function ($public, $system, $context) use($dtd) {
        var_dump($public);
        var_dump($system);
        var_dump($context);
        $f = fopen("php://temp", "r+");
        fwrite($f, $dtd);
        rewind($f);
        return $f;
    }
);

$dd = new DOMDocument;
$r  = $dd->loadXML($xml);

var_dump($dd->validate());
?>
```

Результат виконання цього прикладу:

```
string(10) "-//FOO/BAR"
string(25) "http://example.com/foobar"
array(4) {
    ["directory"]    => NULL
    ["intSubName"]   => NULL
    ["extSubURI"]    => NULL
    ["extSubSystem"] => NULL
}
bool(true)
```

### Дивіться також

-   [libxmldisableentityloader()](function.libxml-disable-entity-loader.html) - Вимкнення можливості завантаження сутностей із зовнішніх джерел