---
navigation:
  - function.imap-check.md: « imap\_check
  - function.imap-close.md: imap\_close »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_clearflag\_full
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_clearflag\_full

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_clearflag\_full — Знімає з повідомлення встановлені прапори

### Опис

```methodsynopsis
imap_clearflag_full(    IMAP\Connection $imap,    string $sequence,    string $flag,    int $options = 0): true
```

Ця функція повідомляє сховище, що необхідно зняти заданий прапор `flag` для зазначеної послідовності повідомлень `sequence`

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`sequence`

Послідовність номерів повідомлень. Ви можете перерахувати номери через кому `X,Y`, або задати діапазон номерів за допомогою двокрапки `X:Y`

`flag`

Прапори, які можна видалити:\\\\Seen", "\\\\Answered", "\\\\Flagged", "\\\\Deleted" та "\\\\Draft" (як визначено в [» RFC2060](http://www.faqs.org/rfcs/rfc2060)) .

`options`

`options` - бітова маска, яка може набувати єдиного значення:

-   \*\*`ST_UID`\*\*- аргумент sequence містить список UID, а не послідовність номерів

### Значення, що повертаються

Функція завжди повертає **`true`**

### Помилки

Викидає виняток [ValueError](class.valueerror.md), если значение параметра`options`недопустимо.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |
| 8.0.0 | Тепер викидається виняток[ValueError](class.valueerror.md) при неприпустимих значеннях параметра `options`. . Раніше виникало попередження та функція повертала логічне значення **`false`** |

### Дивіться також

-   [imap\_setflag\_full()](function.imap-setflag-full.md) \- Встановлює прапори на повідомлення
