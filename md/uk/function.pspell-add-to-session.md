---
navigation:
  - function.pspell-add-to-personal.md: « pspell\_add\_to\_personal
  - function.pspell-check.md: pspell\_check »
  - index.md: PHP Manual
  - ref.pspell.md: Функції Pspell
title: pspell\_add\_to\_session
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pspell\_add\_to\_session

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

pspell\_add\_to\_session — Додає слово до списку слів у поточній сесії

### Опис

```methodsynopsis
pspell_add_to_session(PSpell\Dictionary $dictionary, string $word): bool
```

**pspell\_add\_to\_session()** додає слово до списку слів, асоційованого з поточною сесією. Ця функція дуже схожа на функцію [pspell\_add\_to\_personal()](function.pspell-add-to-personal.md)

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
