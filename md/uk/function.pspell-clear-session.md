---
navigation:
  - function.pspell-check.md: « pspell\_check
  - function.pspell-config-create.md: pspell\_config\_create »
  - index.md: PHP Manual
  - ref.pspell.md: Функції Pspell
title: pspell\_clear\_session
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pspell\_clear\_session

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

pspell\_clear\_session - Очищає поточну сесію

### Опис

```methodsynopsis
pspell_clear_session(PSpell\Dictionary $dictionary): bool
```

**pspell\_clear\_session()** очищує поточну сесію. Поточний список слів очищається, і, наприклад, якщо спробувати зберегти його за допомогою [pspell\_save\_wordlist()](function.pspell-save-wordlist.md), Нічого не трапиться.

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
pspell_config_personal($pspell_config, "/var/dictionaries/custom.pws");
$pspell = pspell_new_config($pspell_config);

pspell_add_to_personal($pspell, "Vlad");
pspell_clear_session($pspell);
pspell_save_wordlist($pspell);    //Слово "Vlad" не будет сохранено
?>
```
