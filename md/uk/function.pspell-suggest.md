Пропонує варіанти виправлення слова

-   [« pspellstorereplacement](function.pspell-store-replacement.html)
    
-   [PSpellDictionary »](class.pspell-dictionary.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Pspell](ref.pspell.html)
    
-   Пропонує варіанти виправлення слова
    

# pspellsuggest

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

pspellsuggest — Пропонує варіанти виправлення слова

### Опис

```methodsynopsis
pspell_suggest(PSpell\Dictionary $dictionary, string $word): array|false
```

**pspellsuggest()** повертає масив можливих варіантів виправлення заданого слова.

### Список параметрів

`dictionary`

Екземпляр [PSpellDictionary](class.pspell-dictionary.html)

`word`

Перевірене слово.

### Значення, що повертаються

Повертає масив можливих варіантів виправлення.

### список змін

| Версия | Описание                                                                                                                                                         |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `dictionary` тепер чекає екземпляр [PSpellDictionary](class.pspell-dictionary.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **pspellsuggest()****

```php
<?php
$pspell = pspell_new("en");

if (!pspell_check($pspell, "testt")) {
    $suggestions = pspell_suggest($pspell, "testt");

    foreach ($suggestions as $suggestion) {
        echo "Возможный вариант исправления: $suggestion<br />";
    }
}
?>
```