---
navigation:
  - function.pspell-config-repl.md: « pspell\_config\_repl
  - function.pspell-config-save-repl.md: pspell\_config\_save\_repl »
  - index.md: PHP Manual
  - ref.pspell.md: Функції Pspell
title: pspell\_config\_runtogether
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pspell\_config\_runtogether

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

pspell\_config\_runtogether — Розглядає об'єднані слова як правильні складні слова

### Опис

```methodsynopsis
pspell_config_runtogether(PSpell\Config $config, bool $allow): bool
```

Функція визначає, чи об'єднані слова розглядатимуться як правильні складні слова. Так, "thecat" буде вважатися правильним складним словом, хоча між артиклем і словом має бути пробіл. Зміна цієї установки впливає лише на результати, що повертаються функцією [pspell\_check()](function.pspell-check.md) [pspell\_suggest()](function.pspell-suggest.md) продовжуватиме видавати варіанти виправлення.

**pspell\_config\_runtogether()** має бути використана для конфігурації перед викликом [pspell\_new\_config()](function.pspell-new-config.md)

### Список параметрів

`config`

Екземпляр [PSpell\\Config](class.pspell-config.md)

`allow`

\*\*`true`\*\*якщо об'єднані слова повинні розглядатися як правильні складні слова, **`false`** в іншому випадку.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`config` тепер чекає екземпляр [PSpell\\Config](class.pspell-config.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pspell\_config\_runtogether()\*\*\*\*

```php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_runtogether($pspell_config, true);
$pspell = pspell_new_config($pspell_config);
pspell_check($pspell, "thecat");
?>
```
