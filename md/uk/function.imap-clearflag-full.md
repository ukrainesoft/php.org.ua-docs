Зняти з повідомлення встановлені прапори

-   [« imapcheck](function.imap-check.html)
    
-   [imapclose »](function.imap-close.html)
    
-   [PHP Manual](index.md)
    
-   [Функции IMAP](ref.imap.md)
    
-   Зняти з повідомлення встановлені прапори
    

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

Екземпляр [IMAPConnection](class.imap-connection.html)

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
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [imapsetflagfull()](function.imap-setflag-full.html) - Встановити прапори на повідомлення