Додає слово до списку слів у поточній сесії

-   [« pspell\_add\_to\_personal](function.pspell-add-to-personal.html)
    
-   [pspell\_check »](function.pspell-check.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Pspell](ref.pspell.html)
    
-   Додає слово до списку слів у поточній сесії
    

# pspelladdтоsession

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

pspelladdтоsession — Додає слово до списку слів у поточній сесії

### Опис

```methodsynopsis
pspell_add_to_session(PSpell\Dictionary $dictionary, string $word): bool
```

**pspelladdтоsession()** додає слово до списку слів, асоційованого з поточною сесією. Ця функція дуже схожа на функцію [pspell\_add\_to\_personal()](function.pspell-add-to-personal.html)

### Список параметрів

`dictionary`

Екземпляр [PSpell\\Dictionary](class.pspell-dictionary.html)

`word`

Слово, що додається.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                           |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `dictionary` тепер чекає екземпляр [PSpell\\Dictionary](class.pspell-dictionary.html); раніше очікувався ресурс ([resource](language.types.resource.html) |