---
navigation:
  - function.pspell-store-replacement.md: « pspellstorereplacement
  - class.pspell-dictionary.md: PSpellDictionary »
  - index.md: PHP Manual
  - ref.pspell.md: Функции Pspell
title: pspellsuggest
---
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

Екземпляр [PSpellDictionary](class.pspell-dictionary.md)

`word`

Перевірене слово.

### Значення, що повертаються

Повертає масив можливих варіантів виправлення.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `dictionary` тепер чекає екземпляр [PSpellDictionary](class.pspell-dictionary.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **pspellsuggest()****

```php
<?php
$pspell = pspell_new("en");

if (!pspell_check($pspell, "testt")) {
    $suggestions = pspell_suggest($pspell, "testt");

    foreach ($suggestions as $suggestion) {
        echo "Возможный вариант исправления: $suggestion<br />";
    }
}
?>
```
