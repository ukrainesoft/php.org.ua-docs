Визначає, чи зберігати список заміщувальних пар разом зі списком слів

-   [« pspell\_config\_runtogether](function.pspell-config-runtogether.html)
    
-   [pspell\_new\_config »](function.pspell-new-config.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Pspell](ref.pspell.html)
    
-   Визначає, чи зберігати список заміщувальних пар разом зі списком слів
    

# pspellconfigsaverepl

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

pspellconfigsaverepl — Визначає, чи зберігати список заміщуваних пар разом зі списком слів

### Опис

```methodsynopsis
pspell_config_save_repl(PSpell\Config $config, bool $save): bool
```

**pspellconfigsaverepl()** визначає, чи буде [pspell\_save\_wordlist()](function.pspell-save-wordlist.html) зберігати пари разом зі списком слів. Зазвичай немає необхідності використовувати цю функцію, оскільки, якщо використовується [pspell\_config\_repl()](function.pspell-config-repl.html), заміщуючі пари будуть збережені [pspell\_save\_wordlist()](function.pspell-save-wordlist.html) у будь-якому випадку, і, якщо вона не використовується, заміщувальні пари не зберігатимуться.

**pspellconfigsaverepl()** має бути використана для конфігурації перед викликом [pspell\_new\_config()](function.pspell-new-config.html)

### Список параметрів

`config`

Екземпляр [PSpell\\Config](class.pspell-config.html)

`save`

**`true`**, якщо заміщувальні пари повинні зберігатися, **`false`** в іншому випадку.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `config` тепер чекає екземпляр [PSpell\\Config](class.pspell-config.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Примітки

> **Зауваження**
> 
> Функція не працюватиме, якщо у вас немає pspell .11.2 і aspell .32.5 або вище.