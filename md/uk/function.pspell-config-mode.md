---
navigation:
  - function.pspell-config-ignore.md: « pspell\_config\_ignore
  - function.pspell-config-personal.md: pspell\_config\_personal »
  - index.md: PHP Manual
  - ref.pspell.md: Функції Pspell
title: pspell\_config\_mode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pspell\_config\_mode

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

pspell\_config\_mode — Змінює режим кількості варіантів виправлення, що повертаються.

### Опис

```methodsynopsis
pspell_config_mode(PSpell\Config $config, int $mode): bool
```

**pspell\_config\_mode()** має бути використана для конфігурації перед викликом [pspell\_new\_config()](function.pspell-new-config.md). Ця функція визначає, скільки варіантів виправлення повертатиме функція [pspell\_suggest()](function.pspell-suggest.md)

### Список параметрів

`config`

Екземпляр [PSpell\\Config](class.pspell-config.md)

`mode`

Параметр mode - це режим, у якому працюватиме перевірка орфографії. Доступно кілька режимів:

-   \*\*`PSPELL_FAST`\*\*- Швидкий режим (найменше варіантів виправлення)
-   \*\*`PSPELL_NORMAL`\*\*- Нормальний режим (більше варіантів виправлення)
-   \*\*`PSPELL_BAD_SPELLERS`\*\*- Повільний режим (багато варіантів виправлення)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`config` тепер чекає екземпляр [PSpell\\Config](class.pspell-config.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** pspell\_config\_mode()\*\*\*\*

```php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_mode($pspell_config, PSPELL_FAST);
$pspell = pspell_new_config($pspell_config);
pspell_check($pspell, "thecat");
?>
```
