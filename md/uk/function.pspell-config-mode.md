Змінює режим кількості варіантів виправлення, що повертаються.

-   [« pspellconfigignore](function.pspell-config-ignore.html)
    
-   [pspellconfigpersonal »](function.pspell-config-personal.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Pspell](ref.pspell.html)
    
-   Змінює режим кількості варіантів виправлення, що повертаються.
    

# pspellconfigmode

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

pspellconfigmode — Змінює режим кількості варіантів виправлення, що повертаються.

### Опис

```methodsynopsis
pspell_config_mode(PSpell\Config $config, int $mode): bool
```

**pspellconfigmode()** має бути використана для конфігурації перед викликом [pspellnewconfig()](function.pspell-new-config.html). Ця функція визначає, скільки варіантів виправлення повертатиме функція [pspellsuggest()](function.pspell-suggest.html)

### Список параметрів

`config`

Екземпляр [PSpellConfig](class.pspell-config.html)

`mode`

Параметр mode - це режим, у якому працюватиме перевірка орфографії. Доступно кілька режимів:

-   **`PSPELL_FAST`** - Швидкий режим (найменше варіантів виправлення)
-   **`PSPELL_NORMAL`** - Нормальний режим (більше варіантів виправлення)
-   **`PSPELL_BAD_SPELLERS`** - Повільний режим (багато варіантів виправлення)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `config` тепер чекає екземпляр [PSpellConfig](class.pspell-config.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **pspellconfigmode()****

```php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_mode($pspell_config, PSPELL_FAST);
$pspell = pspell_new_config($pspell_config);
pspell_check($pspell, "thecat");
?>
```