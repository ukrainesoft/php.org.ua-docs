Визначає, чи зберігати список заміщувальних пар разом зі списком слів

-   [« pspellconfigruntogether](function.pspell-config-runtogether.html)
    
-   [pspellnewconfig »](function.pspell-new-config.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Pspell](ref.pspell.md)
    
-   Визначає, чи зберігати список заміщувальних пар разом зі списком слів
    

# pspellconfigsaverepl

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

pspellconfigsaverepl — Визначає, чи зберігати список заміщуваних пар разом зі списком слів

### Опис

```methodsynopsis
pspell_config_save_repl(PSpell\Config $config, bool $save): bool
```

**pspellconfigsaverepl()** визначає, чи буде [pspellsavewordlist()](function.pspell-save-wordlist.html) зберігати пари разом зі списком слів. Зазвичай немає необхідності використовувати цю функцію, оскільки, якщо використовується [pspellconfigrepl()](function.pspell-config-repl.html), заміщуючі пари будуть збережені [pspellsavewordlist()](function.pspell-save-wordlist.html) у будь-якому випадку, і, якщо вона не використовується, заміщувальні пари не зберігатимуться.

**pspellconfigsaverepl()** має бути використана для конфігурації перед викликом [pspellnewconfig()](function.pspell-new-config.html)

### Список параметрів

`config`

Екземпляр [PSpellConfig](class.pspell-config.html)

`save`

**`true`**, якщо заміщувальні пари повинні зберігатися, **`false`** в іншому випадку.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                           |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `config` тепер чекає екземпляр [PSpellConfig](class.pspell-config.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Примітки

> **Зауваження**
> 
> Функція не працюватиме, якщо у вас немає pspell .11.2 і aspell .32.5 або вище.