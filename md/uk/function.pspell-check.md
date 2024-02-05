---
navigation:
  - function.pspell-add-to-session.md: « pspell\_add\_to\_session
  - function.pspell-clear-session.md: pspell\_clear\_session »
  - index.md: PHP Manual
  - ref.pspell.md: Функції Pspell
title: pspell\_check
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pspell\_check

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

pspell\_check — Перевіряє слово

### Опис

```methodsynopsis
pspell_check(PSpell\Dictionary $dictionary, string $word): bool
```

**pspell\_check()** перевіряє орфографію слова.

### Список параметрів

`dictionary`

Екземпляр [PSpell\\Dictionary](class.pspell-dictionary.md)

`word`

Перевірочне слово.

### Значення, що повертаються

Повертає **`true`**, якщо орфографія вірна, інакше повертає **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`dictionary` тепер чекає екземпляр [PSpell\\Dictionary](class.pspell-dictionary.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pspell\_check()\*\*\*\*

```php
<?php
$pspell = pspell_new("en");

if (pspell_check($pspell, "testt")) {
    echo "Это верное написание";
} else {
    echo "К сожалению, неправильное написание";
}
?>
```
