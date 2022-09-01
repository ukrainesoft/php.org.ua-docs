---
navigation:
  - function.pspell-add-to-personal.html: « pspelladdтоpersonal
  - function.pspell-check.html: pspellcheck »
  - index.md: PHP Manual
  - ref.pspell.md: Функции Pspell
title: pspelladdтоsession
---
# pspelladdтоsession

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

pspelladdтоsession — Додає слово до списку слів у поточній сесії

### Опис

```methodsynopsis
pspell_add_to_session(PSpell\Dictionary $dictionary, string $word): bool
```

**pspelladdтоsession()** додає слово до списку слів, асоційованого з поточною сесією. Ця функція дуже схожа на функцію [pspelladdтоpersonal()](function.pspell-add-to-personal.md)

### Список параметрів

`dictionary`

Екземпляр [PSpellDictionary](class.pspell-dictionary.md)

`word`

Слово, що додається.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `dictionary` тепер чекає екземпляр [PSpellDictionary](class.pspell-dictionary.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
