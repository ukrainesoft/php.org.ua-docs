---
navigation:
  - function.pspell-new.md: « pspellnew
  - function.pspell-store-replacement.md: pspellstorereplacement »
  - index.md: PHP Manual
  - ref.pspell.md: Функции Pspell
title: pspellsavewordlist
---
# pspellsavewordlist

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

pspellsavewordlist — Зберігає персональний список слів у файлі

### Опис

```methodsynopsis
pspell_save_wordlist(PSpell\Dictionary $dictionary): bool
```

**pspellsavewordlist()** зберігає персональний список слів поточної сесії. Розташування файлів для збереження вказується за допомогою [pspellconfigpersonal()](function.pspell-config-personal.md) та (необов'язково) [pspellconfigrepl()](function.pspell-config-repl.md)

### Список параметрів

`dictionary`

Екземпляр [PSpellDictionary](class.pspell-dictionary.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `dictionary` тепер чекає екземпляр [PSpellDictionary](class.pspell-dictionary.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання [pspelladdтоpersonal()](function.pspell-add-to-personal.md)**

```php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_personal($pspell_config, "/tmp/dicts/newdict");
$pspell = pspell_new_config($pspell_config);

pspell_add_to_personal($pspell, "Vlad");
pspell_save_wordlist($pspell);
?>
```

### Примітки

> **Зауваження**
> 
> Функція не працюватиме, якщо у вас немає pspell .11.2 і aspell .32.5 або вище.
