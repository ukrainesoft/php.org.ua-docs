---
navigation:
  - function.imap-scanmailbox.md: « imap\_scanmailbox
  - function.imap-set-quota.md: imap\_set\_quota »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_search
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_search

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_search — Отримує повідомлення, які відповідають заданим критеріям

### Опис

```methodsynopsis
imap_search(    IMAP\Connection $imap,    string $criteria,    int $flags = SE_FREE,    string $charset = ""): array|false
```

Ця функція здійснює пошук у поточній поштовій скриньці, відкритій у потоці IMAP.

Наприклад, щоб знайти всі невідповідні повідомлення надіслані від мами (Mom), потрібно буде використовувати "UNANSWERED FROM mom". Пошук реєстронезалежний. Наведений список критеріїв вилучено із вихідних кодів UW c-client і може бути неповним або не зовсім точним (додатково дивіться [» RFC1176](http://www.faqs.org/rfcs/rfc1176), секція "tag SEARCH search\_criteria").

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`criteria`

Рядок, розділений пробілами, в якому можна використовувати наступні ключові слова. Будь-які аргументи, що складаються з кількох слів, повинні бути поміщені в подвійні лапки (наприклад `FROM "joey smith"`). Результат співпадатиме з усіма заданими в параметрі `criteria`критериями.

-   ALL - повертати всі повідомлення, що відповідають іншим критеріям
-   ANSWERED - повідомлення з виставленим прапором\\\\ANSWERED
-   BCC "string" - повідомлення в полі Bcc: яких є "string"
-   BEFORE "date" - повідомлення з Date: до "date"
-   BODY "string" - повідомлення, що містять "string" в тілі
-   CC "string" - повідомлення у полі Cc: яких є "string"
-   DELETED - видалені повідомлення
-   FLAGGED - повідомлення із встановленим прапором\\\\FLAGGED (іноді називають "Термінове" або "Важливе")
-   FROM "string" - повідомлення в полі From: яких є "string"
-   KEYWORD "string" - повідомлення із ключовим словом "string"
-   NEW - нові повідомлення
-   OLD - старі повідомлення
-   ON "date" - повідомлення з Date: рівним "date"
-   RECENT означає повідомлення з виставленим прапором\\\\RECENT
-   SEEN - прочитані повідомлення (встановлений прапор\\\\SEEN)
-   SINCE "date" - повідомлення з Date: після "date"
-   SUBJECT "string" - повідомлення в полі Subject: яких є "string"
-   TEXT "string" - повідомлення з текстом "string"
-   TO "string" - повідомлення в полі To: яких є присутнім "string"
-   UNANSWERED - невідповідні повідомлення
-   UNDELETED - не видалені повідомлення
-   UNFLAGGED - повідомлення без встановлених прапорів
-   UNKEYWORD "string" - повідомлення, що не мають ключового слова "string"
-   UNSEEN - непрочитані повідомлення

`flags`

Коректні значення `flags` - це **`SE_UID`**, що призведе до того, що у поверненому масиві замість номерів повідомлень будуть міститися їх UID.

`charset`

Кодування MIME, у якому відбуватиметься пошук.

### Значення, що повертаються

Повертає номери повідомлень або їх UID.

Повертає **`false`**, якщо повідомлення не знайдені, або критерії зазначені в `criteria` некоректні.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Приклади

**Приклад #1 Приклад використання** imap\_search()\*\*\*\*

```php
<?php
$imap   = imap_open('{imap.example.com:993/imap/ssl}INBOX', 'foo@example.com', 'pass123', OP_READONLY);

$some   = imap_search($imap, 'SUBJECT "HOWTO be Awesome" SINCE "8 August 2008"', SE_UID);
$msgnos = imap_search($imap, 'ALL');
$uids   = imap_search($imap, 'ALL', SE_UID);

print_r($some);
print_r($msgnos);
print_r($uids);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => 4
    [1] => 6
    [2] => 11
)
Array
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
    [4] => 5
    [5] => 6
)
Array
(
    [0] => 1
    [1] => 4
    [2] => 6
    [3] => 8
    [4] => 11
    [5] => 12
)
```

### Дивіться також

-   [imap\_listscan()](function.imap-listscan.md) \- Отримує список поштових скриньок, імена яких містять заданий рядок
