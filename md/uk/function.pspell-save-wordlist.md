Зберігає персональний список слів у файлі

-   [« pspell\_new](function.pspell-new.html)
    
-   [pspell\_store\_replacement »](function.pspell-store-replacement.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Pspell](ref.pspell.html)
    
-   Зберігає персональний список слів у файлі
    

# pspellsavewordlist

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

pspellsavewordlist — Зберігає персональний список слів у файлі

### Опис

```methodsynopsis
pspell_save_wordlist(PSpell\Dictionary $dictionary): bool
```

**pspellsavewordlist()** зберігає персональний список слів поточної сесії. Розташування файлів для збереження вказується за допомогою [pspell\_config\_personal()](function.pspell-config-personal.html) та (необов'язково) [pspell\_config\_repl()](function.pspell-config-repl.html)

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