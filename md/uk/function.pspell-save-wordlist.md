---
navigation:
  - function.pspell-new.md: « pspell\_new
  - function.pspell-store-replacement.md: pspell\_store\_replacement »
  - index.md: PHP Manual
  - ref.pspell.md: Функції Pspell
title: pspell\_save\_wordlist
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pspell\_save\_wordlist

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

pspell\_save\_wordlist — Зберігає персональний список слів у файлі

### Опис

```methodsynopsis
pspell_save_wordlist(PSpell\Dictionary $dictionary): bool
```

**pspell\_save\_wordlist()** зберігає персональний список слів поточної сесії. Розташування файлів для збереження вказується за допомогою [pspell\_config\_personal()](function.pspell-config-personal.md) та (необов'язково) [pspell\_config\_repl()](function.pspell-config-repl.md)

### Список параметрів

`dictionary`

Екземпляр [PSpell\\Dictionary](class.pspell-dictionary.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`dictionary` тепер чекає екземпляр [PSpell\\Dictionary](class.pspell-dictionary.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад использования[pspell\_add\_to\_personal()](function.pspell-add-to-personal.md)**

```php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_personal($pspell_config, "/tmp/dicts/newdict");
$pspell = pspell_new_config($pspell_config);

pspell_add_to_personal($pspell, "Vlad");
pspell_save_wordlist($pspell);
?>
```

### Примітки

> **Зауваження** :
> 
> Функція не працюватиме, якщо у вас немає pspell .11.2 і aspell .32.5 або вище.
