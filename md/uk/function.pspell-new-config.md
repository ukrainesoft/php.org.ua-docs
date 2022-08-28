Завантажує новий словник із установками на основі заданої конфігурації

-   [« pspell\_config\_save\_repl](function.pspell-config-save-repl.html)
    
-   [pspell\_new\_personal »](function.pspell-new-personal.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Pspell](ref.pspell.html)
    
-   Завантажує новий словник із установками на основі заданої конфігурації
    

# pspellnewconfig

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

pspellnewconfig — Завантажує новий словник із установками на основі заданої конфігурації

### Опис

```methodsynopsis
pspell_new_config(PSpell\Config $config): PSpell\Dictionary|false
```

**pspellnewconfig()** відкриває новий словник з параметрами, заданими в `config`, створеної за допомогою [pspell\_config\_create()](function.pspell-config-create.html) та модифікованою за допомогою функцій **pspellconfig**. Цей метод дає найбільшу гнучкість і має всі функціональні можливості, що надаються [pspell\_new()](function.pspell-new.html) і [pspell\_new\_personal()](function.pspell-new-personal.html)

### Список параметрів

`config`

Параметр `config` - це параметр повернутий функцією [pspell\_config\_create()](function.pspell-config-create.html) після того, як конфігурацію було створено.

### Значення, що повертаються

Повертає екземпляр [PSpell\\Dictionary](class.pspell-dictionary.html) у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                               |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `config` тепер чекає екземпляр [PSpell\\Config](class.pspell-config.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|        | Повертає екземпляр [PSpell\\Dictionary](class.pspell-dictionary.html); раніше повертався ресурс ([resource](language.types.resource.html)              |

### Приклади

**Приклад #1 Приклад використання **pspellnewconfig()****

```php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_personal($pspell_config, "/var/dictionaries/custom.pws");
pspell_config_repl($pspell_config, "/var/dictionaries/custom.repl");
$pspell = pspell_new_config($pspell_config);
?>
```