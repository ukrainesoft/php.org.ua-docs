Очищує поточну сесію

-   [« pspell\_check](function.pspell-check.html)
    
-   [pspell\_config\_create »](function.pspell-config-create.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Pspell](ref.pspell.html)
    
-   Очищує поточну сесію
    

# pspellclearsession

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

pspellclearsession - Очищає поточну сесію

### Опис

```methodsynopsis
pspell_clear_session(PSpell\Dictionary $dictionary): bool
```

**pspellclearsession()** очищує поточну сесію. Поточний список слів очищається, і, наприклад, якщо спробувати зберегти його за допомогою [pspell\_save\_wordlist()](function.pspell-save-wordlist.html), Нічого не трапиться.

### Список параметрів

`dictionary`

Екземпляр [PSpell\\Dictionary](class.pspell-dictionary.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `dictionary` тепер чекає екземпляр [PSpell\\Dictionary](class.pspell-dictionary.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання [pspell\_add\_to\_personal()](function.pspell-add-to-personal.html)**

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