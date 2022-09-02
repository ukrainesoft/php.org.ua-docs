---
navigation:
  - function.imap-check.md: « imapcheck
  - function.imap-close.md: imapclose »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imapclearflagfull
---
# imapclearflagfull

(PHP 4, PHP 5, PHP 7, PHP 8)

imapclearflagfull — Зняти з повідомлення встановлені прапори

### Опис

```methodsynopsis
imap_clearflag_full(    IMAP\Connection $imap,    string $sequence,    string $flag,    int $options = 0): bool
```

Ця функція повідомляє сховище, що необхідно зняти заданий прапор `flag` для зазначеної послідовності повідомлень `sequence`

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.md)

`sequence`

Послідовність номерів повідомлень. Ви можете перерахувати номери через кому `X,Y`, або задати діапазон номерів за допомогою двокрапки `X:Y`

`flag`

Прапори, які можна видалити:Seen", "Answered", "Flagged", "Deleted" та "Draft" (як визначено в [» RFC2060](http://www.faqs.org/rfcs/rfc2060)

`options`

`options` - бітова маска, яка може набувати єдиного значення:

-   **`ST_UID`** - аргумент sequence містить список UID, а не послідовність номерів

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [imapsetflagfull()](function.imap-setflag-full.md) - Встановити прапори на повідомлення
