Додає слово до персонального списку слів

-   [« Функции Pspell](ref.pspell.html)
    
-   [pspelladdтоsession »](function.pspell-add-to-session.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Pspell](ref.pspell.html)
    
-   Додає слово до персонального списку слів
    

# pspelladdтоpersonal

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

pspelladdтоpersonal — Додає слово до персонального списку слів

### Опис

```methodsynopsis
pspell_add_to_personal(PSpell\Dictionary $dictionary, string $word): bool
```

**pspelladdтоpersonal()** додає слово до персонального списку слів. Якщо ви використовували [pspellnewconfig()](function.pspell-new-config.html) разом з [pspellconfigpersonal()](function.pspell-config-personal.html) для відкриття словника, ви можете зберегти список слів пізніше за допомогою [pspellsavewordlist()](function.pspell-save-wordlist.html)

### Список параметрів

`dictionary`

Екземпляр [PSpellDictionary](class.pspell-dictionary.html)

`word`

Слово, що додається.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                         |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `dictionary` тепер чекає екземпляр [PSpellDictionary](class.pspell-dictionary.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **pspelladdтоpersonal()****

```php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_personal($pspell_config, "/var/dictionaries/custom.pws");
$pspell = pspell_new_config($pspell_config);

pspell_add_to_personal($pspell, "Vlad");
pspell_save_wordlist($pspell);
?>
```

### Примітки

> **Зауваження**
> 
> Функція не працюватиме, якщо у вас немає pspell .11.2 і aspell .32.5 або вище.