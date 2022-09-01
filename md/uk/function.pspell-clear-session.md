---
navigation:
  - function.pspell-check.html: « pspellcheck
  - function.pspell-config-create.html: pspellconfigcreate »
  - index.md: PHP Manual
  - ref.pspell.md: Функции Pspell
title: pspellclearsession
---
# pspellclearsession

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

pspellclearsession - Очищає поточну сесію

### Опис

```methodsynopsis
pspell_clear_session(PSpell\Dictionary $dictionary): bool
```

**pspellclearsession()** очищує поточну сесію. Поточний список слів очищається, і, наприклад, якщо спробувати зберегти його за допомогою [pspellsavewordlist()](function.pspell-save-wordlist.md), Нічого не трапиться.

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
pspell_config_personal($pspell_config, "/var/dictionaries/custom.pws");
$pspell = pspell_new_config($pspell_config);

pspell_add_to_personal($pspell, "Vlad");
pspell_clear_session($pspell);
pspell_save_wordlist($pspell);    //Слово "Vlad" не будет сохранено
?>
```
