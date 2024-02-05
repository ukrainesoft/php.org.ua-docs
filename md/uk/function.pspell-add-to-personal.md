---
navigation:
  - ref.pspell.md: « Функції Pspell
  - function.pspell-add-to-session.md: pspell\_add\_to\_session »
  - index.md: PHP Manual
  - ref.pspell.md: Функції Pspell
title: pspell\_add\_to\_personal
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pspell\_add\_to\_personal

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

pspell\_add\_to\_personal — Додає слово до персонального списку слів

### Опис

```methodsynopsis
pspell_add_to_personal(PSpell\Dictionary $dictionary, string $word): bool
```

**pspell\_add\_to\_personal()** додає слово до персонального списку слів. Якщо ви використовували [pspell\_new\_config()](function.pspell-new-config.md)вместе с[pspell\_config\_personal()](function.pspell-config-personal.md) для відкриття словника, ви можете зберегти список слів пізніше за допомогою [pspell\_save\_wordlist()](function.pspell-save-wordlist.md)

### Список параметрів

`dictionary`

Екземпляр [PSpell\\Dictionary](class.pspell-dictionary.md)

`word`

Слово, що додається.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`dictionary` тепер чекає екземпляр [PSpell\\Dictionary](class.pspell-dictionary.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** pspell\_add\_to\_personal()\*\*\*\*

```php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_personal($pspell_config, "/var/dictionaries/custom.pws");
$pspell = pspell_new_config($pspell_config);

pspell_add_to_personal($pspell, "Vlad");
pspell_save_wordlist($pspell);
?>
```

### Примітки

> **Зауваження** :
> 
> Функція не працюватиме, якщо у вас немає pspell .11.2 і aspell .32.5 або вище.
