Ігнорує слова довжиною менше N символів

-   [« pspellconfigdictdir](function.pspell-config-dict-dir.html)
    
-   [pspellconfigmode »](function.pspell-config-mode.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Pspell](ref.pspell.md)
    
-   Ігнорує слова довжиною менше N символів
    

# pspellconfigignore

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

pspellconfigignore — Ігнорує слова довжиною менше N символів

### Опис

```methodsynopsis
pspell_config_ignore(PSpell\Config $config, int $min_length): bool
```

**pspellconfigignore()** має бути використана для конфігурації перед викликом [pspellnewconfig()](function.pspell-new-config.html). Ця функція дозволяє пропускати короткі слова під час перевірки орфографії.

### Список параметрів

`config`

Екземпляр [PSpellConfig](class.pspell-config.html)

`min_length`

Слова довжиною менше `min_length` символів буде пропущено.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `config` тепер чекає екземпляр [PSpellConfig](class.pspell-config.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **pspellconfigignore()****

```php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_ignore($pspell_config, 5);
$pspell = pspell_new_config($pspell_config);
pspell_check($pspell, "abcd");    //Сообщение об ошибке не будет сгенерировано
?>
```