---
navigation:
  - function.pspell-config-personal.md: « pspell\_config\_personal
  - function.pspell-config-runtogether.md: pspell\_config\_runtogether »
  - index.md: PHP Manual
  - ref.pspell.md: Функції Pspell
title: pspell\_config\_repl
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pspell\_config\_repl

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

pspell\_config\_repl — Встановлює файл, який містить заміщувальні пари

### Опис

```methodsynopsis
pspell_config_repl(PSpell\Config $config, string $filename): bool
```

Встановлює файл, що містить пари, що заміщають.

Заміщаючі пари підвищують якість перевірки орфографії. Коли слово написано з помилками, а правильний варіант не знайдено у списку, [pspell\_store\_replacement()](function.pspell-store-replacement.md) може бути використана для того, щоб зберегти заміщувальну пару, а [pspell\_save\_wordlist()](function.pspell-save-wordlist.md) - щоб зберегти список слів разом із заміщувальною парою.

**pspell\_config\_repl()** має бути використана для конфігурації перед викликом [pspell\_new\_config()](function.pspell-new-config.md)

### Список параметрів

`config`

Екземпляр [PSpell\\Config](class.pspell-config.md)

`filename`

Файл має бути доступним для запису будь-кому, хто запускає PHP (наприклад, nobody).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`config` тепер чекає екземпляр [PSpell\\Config](class.pspell-config.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** pspell\_config\_repl()\*\*\*\*

```php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_personal($pspell_config, "/var/dictionaries/custom.pws");
pspell_config_repl($pspell_config, "/var/dictionaries/custom.repl");
$pspell = pspell_new_config($pspell_config);
pspell_check($pspell, "thecat");
?>
```

### Примітки

> **Зауваження** :
> 
> Функція не працюватиме, якщо у вас немає pspell .11.2 і aspell .32.5 або вище.
