Встановлює файл, який містить заміщувальні пари

-   [« pspellconfigpersonal](function.pspell-config-personal.html)
    
-   [pspellconfigruntogether »](function.pspell-config-runtogether.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Pspell](ref.pspell.md)
    
-   Встановлює файл, який містить заміщувальні пари
    

# pspellconfigrepl

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

pspellconfigrepl — Встановлює файл, який містить заміщувальні пари

### Опис

```methodsynopsis
pspell_config_repl(PSpell\Config $config, string $filename): bool
```

Встановлює файл, що містить пари, що заміщають.

Заміщаючі пари підвищують якість перевірки орфографії. Коли слово написано з помилками, а правильний варіант не знайдено у списку, [pspellstorereplacement()](function.pspell-store-replacement.html) може бути використана для того, щоб зберегти заміщувальну пару, а [pspellsavewordlist()](function.pspell-save-wordlist.html) - щоб зберегти список слів разом із заміщувальною парою.

**pspellconfigrepl()** має бути використана для конфігурації перед викликом [pspellnewconfig()](function.pspell-new-config.html)

### Список параметрів

`config`

Екземпляр [PSpellConfig](class.pspell-config.html)

`filename`

Файл має бути доступним для запису будь-кому, хто запускає PHP (наприклад, nobody).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `config` тепер чекає екземпляр [PSpellConfig](class.pspell-config.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **pspellconfigrepl()****

```php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_personal($pspell_config, "/var/dictionaries/custom.pws");
pspell_config_repl($pspell_config, "/var/dictionaries/custom.repl");
$pspell = pspell_new_config($pspell_config);
pspell_check($pspell, "thecat");
?>
```

### Примітки

> **Зауваження**
> 
> Функція не працюватиме, якщо у вас немає pspell .11.2 і aspell .32.5 або вище.