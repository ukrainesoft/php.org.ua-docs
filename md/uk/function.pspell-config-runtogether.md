---
navigation:
  - function.pspell-config-repl.md: « pspellconfigrepl
  - function.pspell-config-save-repl.md: pspellconfigsaverepl »
  - index.md: PHP Manual
  - ref.pspell.md: Функции Pspell
title: pspellconfigruntogether
---
# pspellconfigruntogether

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

pspellconfigruntogether - Розглядає об'єднані слова як правильні складні слова

### Опис

```methodsynopsis
pspell_config_runtogether(PSpell\Config $config, bool $allow): bool
```

Функція визначає, чи об'єднані слова розглядатимуться як правильні складні слова. Так, "thecat" буде вважатися правильним складним словом, хоча між артиклем і словом має бути пробіл. Зміна цієї установки впливає лише на результати, що повертаються функцією [pspellcheck()](function.pspell-check.md) [pspellsuggest()](function.pspell-suggest.md) продовжуватиме видавати варіанти виправлення.

**pspellconfigruntogether()** має бути використана для конфігурації перед викликом [pspellnewconfig()](function.pspell-new-config.md)

### Список параметрів

`config`

Екземпляр [PSpellConfig](class.pspell-config.md)

`allow`

\*\*`true`\*\*якщо об'єднані слова повинні розглядатися як правильні складні слова, **`false`** в іншому випадку.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `config` тепер чекає екземпляр [PSpellConfig](class.pspell-config.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **pspellconfigruntogether()****

```php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_runtogether($pspell_config, true);
$pspell = pspell_new_config($pspell_config);
pspell_check($pspell, "thecat");
?>
```
