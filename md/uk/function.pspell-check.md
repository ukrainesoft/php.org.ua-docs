---
navigation:
  - function.pspell-add-to-session.html: « pspelladdтоsession
  - function.pspell-clear-session.html: pspellclearsession »
  - index.md: PHP Manual
  - ref.pspell.md: Функции Pspell
title: pspellcheck
---
# pspellcheck

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

pspellcheck — Перевіряє слово

### Опис

```methodsynopsis
pspell_check(PSpell\Dictionary $dictionary, string $word): bool
```

**pspellcheck()** перевіряє орфографію слова.

### Список параметрів

`dictionary`

Екземпляр [PSpellDictionary](class.pspell-dictionary.html)

`word`

Перевірене слово.

### Значення, що повертаються

Повертає **`true`**, якщо орфографія вірна, інакше повертає **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `dictionary` тепер чекає екземпляр [PSpellDictionary](class.pspell-dictionary.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **pspellcheck()****

```php
<?php
$pspell = pspell_new("en");

if (pspell_check($pspell, "testt")) {
    echo "Это верное написание";
} else {
    echo "К сожалению, неправильное написание";
}
?>
```
