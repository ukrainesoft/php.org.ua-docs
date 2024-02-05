---
navigation:
  - function.imap-setacl.md: « imap\_setacl
  - function.imap-sort.md: imap\_sort »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_setflag\_full
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_setflag\_full

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_setflag\_full — Встановлює прапори на повідомлення

### Опис

```methodsynopsis
imap_setflag_full(    IMAP\Connection $imap,    string $sequence,    string $flag,    int $options = 0): true
```

Повідомляє сервер, що треба додати прапор `flag` до набору прапорів, заданих у `sequence` повідомлень.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`sequence`

Послідовність номерів повідомлень. Ви можете перерахувати кілька повідомлень, використовуючи як роздільник кому (`X,Y`), або задати інтервал повідомлень за допомогою двокрапки `X:Y`

`flag`

Прапори, які можна встановити: `\Seen` `\Answered` `\Flagged` `\Deleted`и`\Draft`, как определено в[» RFC2060](http://www.faqs.org/rfcs/rfc2060)

`options`

Бітова маска, яка може приймати лише одне значення:

-   \*\*`ST_UID`\*\*- Послідовність повідомлень задана не їх номерами, а за допомогою UID

### Значення, що повертаються

Функція завжди повертає **`true`**

### Помилки

Викидає виняток [ValueError](class.valueerror.md), если значение параметра`options`недопустимо.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |
| 8.0.0 | Тепер викидається виняток[ValueError](class.valueerror.md) при неприпустимих значеннях параметра `options`. . Раніше виникало попередження та функція повертала логічне значення **`false`** |

### Приклади

**Приклад #1 Приклад використання** imap\_setflag\_full()\*\*\*\*

```php
<?php
$mbox = imap_open("{imap.example.org:143}", "username", "password")
     or die("не удалось подключиться: " . imap_last_error());

$status = imap_setflag_full($mbox, "2,5", "\\Seen \\Flagged");

echo gettype($status) . "\n";
echo $status . "\n";

imap_close($mbox);
?>
```

### Дивіться також

-   [imap\_clearflag\_full()](function.imap-clearflag-full.md) \- Знімає з повідомлення встановлені прапори
