---
navigation:
  - function.pspell-config-mode.md: « pspell\_config\_mode
  - function.pspell-config-repl.md: pspell\_config\_repl »
  - index.md: PHP Manual
  - ref.pspell.md: Функції Pspell
title: pspell\_config\_personal
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pspell\_config\_personal

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

pspell\_config\_personal — Встановлює файл, який містить персональний список слів

### Опис

```methodsynopsis
pspell_config_personal(PSpell\Config $config, string $filename): bool
```

Встановлює файл, який містить список персональних слів. Персональний список слів буде завантажено та використано на додаток до стандартного після того, як ви викликаєте [pspell\_new\_config()](function.pspell-new-config.md). Це той самий файл, в який функція [pspell\_save\_wordlist()](function.pspell-save-wordlist.md) збереже персональний перелік слів.

**pspell\_config\_personal()** має бути використана для конфігурації перед викликом [pspell\_new\_config()](function.pspell-new-config.md)

### Список параметрів

`config`

Екземпляр [PSpell\\Config](class.pspell-config.md)

`filename`

Персональний перелік слів. Якщо файл не існує, його буде створено. Файл має бути доступним для запису будь-кому, хто запускає PHP (наприклад, nobody).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`config` тепер чекає екземпляр [PSpell\\Config](class.pspell-config.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pspell\_config\_personal()\*\*\*\*

```php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_personal($pspell_config, "/var/dictionaries/custom.pws");
$pspell = pspell_new_config($pspell_config);
pspell_check($pspell, "thecat");
?>
```

### Примітки

> **Зауваження** :
> 
> Функція не працюватиме, якщо у вас немає pspell .11.2 і aspell .32.5 або вище.
