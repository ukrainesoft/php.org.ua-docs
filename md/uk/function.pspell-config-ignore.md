---
navigation:
  - function.pspell-config-dict-dir.md: « pspell\_config\_dict\_dir
  - function.pspell-config-mode.md: pspell\_config\_mode »
  - index.md: PHP Manual
  - ref.pspell.md: Функції Pspell
title: pspell\_config\_ignore
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pspell\_config\_ignore

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

pspell\_config\_ignore — Ігнорує слова довжиною менше N символів

### Опис

```methodsynopsis
pspell_config_ignore(PSpell\Config $config, int $min_length): bool
```

**pspell\_config\_ignore()** має бути використана для конфігурації перед викликом [pspell\_new\_config()](function.pspell-new-config.md). Ця функція дозволяє пропускати короткі слова під час перевірки орфографії.

### Список параметрів

`config`

Екземпляр [PSpell\\Config](class.pspell-config.md)

`min_length`

Слова завдовжки менше `min_length` символів буде пропущено.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`config` тепер чекає екземпляр [PSpell\\Config](class.pspell-config.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pspell\_config\_ignore()\*\*\*\*

```php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_ignore($pspell_config, 5);
$pspell = pspell_new_config($pspell_config);
pspell_check($pspell, "abcd");    //Сообщение об ошибке не будет сгенерировано
?>
```
