---
navigation:
  - function.pspell-store-replacement.md: « pspell\_store\_replacement
  - class.pspell-dictionary.md: PSpell\\Dictionary »
  - index.md: PHP Manual
  - ref.pspell.md: Функції Pspell
title: pspell\_suggest
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pspell\_suggest

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

pspell\_suggest — Пропонує варіанти виправлення слова

### Опис

```methodsynopsis
pspell_suggest(PSpell\Dictionary $dictionary, string $word): array|false
```

**pspell\_suggest()** повертає масив можливих варіантів виправлення заданого слова.

### Список параметрів

`dictionary`

Екземпляр [PSpell\\Dictionary](class.pspell-dictionary.md)

`word`

Перевірочне слово.

### Значення, що повертаються

Повертає масив можливих варіантів виправлення.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`dictionary` тепер чекає екземпляр [PSpell\\Dictionary](class.pspell-dictionary.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pspell\_suggest()\*\*\*\*

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
