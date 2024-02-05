---
navigation:
  - function.libxml-get-last-error.md: « libxml\_get\_last\_error
  - function.libxml-set-streams-context.md: libxml\_set\_streams\_context »
  - index.md: PHP Manual
  - ref.libxml.md: Функції libxml
title: libxml\_set\_external\_entity\_loader
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# libxml\_set\_external\_entity\_loader

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

libxml\_set\_external\_entity\_loader — Змінити завантажувач за умовчанням для зовнішніх об'єктів

### Опис

```methodsynopsis
libxml_set_external_entity_loader(?callable $resolver_function): bool
```

Зміна стандартного завантажувача для зовнішніх об'єктів. Можна використовувати для придушення розширення довільних зовнішніх сутностей, щоб уникнути XXE-атак, навіть якщо для відповідної операції встановлено значення **`LIBXML_NOENT`**. Зазвичай це краще, ніж виклик [libxml\_disable\_entity\_loader()](function.libxml-disable-entity-loader.md)

### Список параметрів

`resolver_function`

Callback-функція ([callable](language.types.callable.md)) з наступною сигнатурою:

```methodsynopsis
resolver(?string $public_id, string $system_id, array $context): resource|string|null
```

`public_id`

Громадський ідентифікатор.

`system_id`

Системний ідентифікатор.

`context`

Масив із чотирьох елементів: `"directory"` `"intSubName"` `"extSubURI"`и`"extSubSystem"`

Ця callback-функція повинна повертати ресурс ([resource](language.types.resource.md)) або рядок (string) з якого можна відкрити ресурс. Якщо повертається **`null`**, роздільна здатність посилання на сутність завершиться помилкою.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** libxml\_set\_external\_entity\_loader()\*\*\*\*

```php
<?php
$xml = <<<XML
<!DOCTYPE foo PUBLIC "-//FOO/BAR" "http://example.com/foobar">
<foo>bar</foo>
XML;

$dtd = <<<DTD
<!ELEMENT foo (#PCDATA)>
DTD;

libxml_set_external_entity_loader(
    function ($public, $system, $context) use($dtd) {
        var_dump($public);
        var_dump($system);
        var_dump($context);
        $f = fopen("php://temp", "r+");
        fwrite($f, $dtd);
        rewind($f);
        return $f;
    }
);

$dd = new DOMDocument;
$r  = $dd->loadXML($xml);

var_dump($dd->validate());
?>
```

Результат виконання наведеного прикладу:

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

-   [libxml\_disable\_entity\_loader()](function.libxml-disable-entity-loader.md) \- Вимкнення можливості завантаження сутностей із зовнішніх джерел
-   [libxml\_get\_external\_entity\_loader()](function.libxml-get-external-entity-loader.md) \- Отримує поточний зовнішній завантажувач сутностей
