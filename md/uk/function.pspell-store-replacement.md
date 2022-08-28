Зберігає заміщувальну пару для слова

-   [« pspell\_save\_wordlist](function.pspell-save-wordlist.html)
    
-   [pspell\_suggest »](function.pspell-suggest.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Pspell](ref.pspell.html)
    
-   Зберігає заміщувальну пару для слова
    

# pspellstorereplacement

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

pspellstorereplacement — Зберігає заміщувальну пару для слова

### Опис

```methodsynopsis
pspell_store_replacement(PSpell\Dictionary $dictionary, string $misspelled, string $correct): bool
```

**pspellstorereplacement()** зберігає заміщувальну пару для слова, так що заміна пізніше може бути повернена функцією [pspell\_suggest()](function.pspell-suggest.html). Щоб використати переваги цієї функції, слід відкрити словник за допомогою [pspell\_new\_personal()](function.pspell-new-personal.html). Щоб назавжди зберегти пару, що заміщає, необхідно використовувати [pspell\_config\_personal()](function.pspell-config-personal.html) і [pspell\_config\_repl()](function.pspell-config-repl.html) для того, щоб вказати шлях, куди зберегти списки слів, а потім скористатися [pspell\_save\_wordlist()](function.pspell-save-wordlist.html) для запису змін на диск.

### Список параметрів

`dictionary`

Екземпляр [PSpell\\Dictionary](class.pspell-dictionary.html)

`misspelled`

Слово з помилкою.

`correct`

Виправлене написання для слова з помилкою (`misspelled`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                           |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `dictionary` тепер чекає екземпляр [PSpell\\Dictionary](class.pspell-dictionary.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **pspellstorereplacement()****

```php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_personal($pspell_config, "/var/dictionaries/custom.pws");
pspell_config_repl($pspell_config, "/var/dictionaries/custom.repl");
$pspell = pspell_new_config($pspell_config);

pspell_store_replacement($pspell, $misspelled, $correct);
pspell_save_wordlist($pspell);
?>
```

### Примітки

> **Зауваження**
> 
> Функція не працюватиме, якщо у вас немає pspell .11.2 і aspell .32.5 або вище.