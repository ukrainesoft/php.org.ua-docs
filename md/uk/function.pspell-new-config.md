---
navigation:
  - function.pspell-config-save-repl.md: « pspell\_config\_save\_repl
  - function.pspell-new-personal.md: pspell\_new\_personal »
  - index.md: PHP Manual
  - ref.pspell.md: Функції Pspell
title: pspell\_new\_config
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pspell\_new\_config

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

pspell\_new\_config — Завантажує новий словник із установками на основі заданої конфігурації

### Опис

```methodsynopsis
pspell_new_config(PSpell\Config $config): PSpell\Dictionary|false
```

**pspell\_new\_config()** відкриває новий словник з параметрами, заданими в `config`, створеної за допомогою [pspell\_config\_create()](function.pspell-config-create.md) та модифікованою за допомогою функцій **pspell\_config\_\*()**. Цей метод дає найбільшу гнучкість і має всі функціональні можливості, що надаються [pspell\_new()](function.pspell-new.md) і [pspell\_new\_personal()](function.pspell-new-personal.md)

### Список параметрів

`config`

Параметр`config` - це параметр повернутий функцією [pspell\_config\_create()](function.pspell-config-create.md) після того, як конфігурацію було створено.

### Значення, що повертаються

Повертає екземпляр [PSpell\\Dictionary](class.pspell-dictionary.md) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`config` тепер чекає екземпляр [PSpell\\Config](class.pspell-config.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
| 8.1.0 | Повертає екземпляр [PSpell\\Dictionary](class.pspell-dictionary.md); раніше повертався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pspell\_new\_config()\*\*\*\*

```php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_personal($pspell_config, "/var/dictionaries/custom.pws");
pspell_config_repl($pspell_config, "/var/dictionaries/custom.repl");
$pspell = pspell_new_config($pspell_config);
?>
```
