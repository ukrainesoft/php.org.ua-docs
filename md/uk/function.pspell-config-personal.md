---
navigation:
  - function.pspell-config-mode.md: « pspellconfigmode
  - function.pspell-config-repl.md: pspellconfigrepl »
  - index.md: PHP Manual
  - ref.pspell.md: Функции Pspell
title: pspellconfigpersonal
---
# pspellconfigpersonal

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

pspellconfigpersonal — Встановлює файл, який містить персональний список слів

### Опис

```methodsynopsis
pspell_config_personal(PSpell\Config $config, string $filename): bool
```

Встановлює файл, який містить список персональних слів. Персональний список слів буде завантажено та використано на додаток до стандартного після того, як ви викликаєте [pspellnewconfig()](function.pspell-new-config.md). Це той самий файл, в який функція [pspellsavewordlist()](function.pspell-save-wordlist.md) збереже персональний перелік слів.

**pspellconfigpersonal()** має бути використана для конфігурації перед викликом [pspellnewconfig()](function.pspell-new-config.md)

### Список параметрів

`config`

Екземпляр [PSpellConfig](class.pspell-config.md)

`filename`

Персональний перелік слів. Якщо файл не існує, його буде створено. Файл має бути доступним для запису будь-кому, хто запускає PHP (наприклад, nobody).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `config` тепер чекає екземпляр [PSpellConfig](class.pspell-config.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **pspellconfigpersonal()****

```php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_personal($pspell_config, "/var/dictionaries/custom.pws");
$pspell = pspell_new_config($pspell_config);
pspell_check($pspell, "thecat");
?>
```

### Примітки

> **Зауваження**
> 
> Функція не працюватиме, якщо у вас немає pspell .11.2 і aspell .32.5 або вище.
