---
navigation:
  - function.imap-expunge.md: « imap\_expunge
  - function.imap-fetchbody.md: imap\_fetchbody »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_fetch\_overview
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_fetch\_overview

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_fetch\_overview — Оглядає інформацію із заголовків повідомлень

### Опис

```methodsynopsis
imap_fetch_overview(IMAP\Connection $imap, string $sequence, int $flags = 0): array|false
```

Ця функція читає заголовки повідомлень, заданих у параметрі `sequence`, та повертає оглядову інформацію про їх зміст.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`sequence`

Послідовність номерів повідомлень. Ви можете перерахувати кілька повідомлень, використовуючи як роздільник кому (`X,Y`), або задати інтервал повідомлень за допомогою двокрапки `X:Y`

`flags`

Параметр`sequence` має містити номери повідомлень. Якщо ви хочете задати в ньому їх UID, цей параметр необхідно задати значенням **`FT_UID`**

### Значення, що повертаються

Повертає масив об'єктів, кожен із яких визначає заголовок одного повідомлення. Об'єкти містять відповідні властивості, тільки якщо вони присутні. Можливі властивості:

-   `subject`\- Тема листа
-   `from`\- хто його послав
-   `to`\- одержувач
-   `date`\- коли воно було надіслано
-   `message_id`\- Ідентифікатор повідомлення
-   `references`\- є посиланням на цей ідентифікатор повідомлення
-   `in_reply_to`\- є відповіддю на лист із цим ідентифікатором
-   `size`\- Розмір у байтах
-   `uid`\- UID повідомлення у скриньці
-   `msgno`\- номер повідомлення у скриньці
-   `recent`\- лист позначений як новий
-   `flagged` - це повідомлення позначено (зазвичай є ознакою "важливості")
-   `answered`\- повідомлення позначене як відповідь
-   `deleted`\- позначено для видалення
-   `seen`\- позначено як прочитане
-   `draft`\- позначено як чернетка
-   `udate`\- тимчасова мітка UNIX дати отримання

Функція повертає \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Приклади

**Приклад #1 Приклад використання** imap\_fetch\_overview()\*\*\*\*

```php
<?php
$mbox = imap_open("{imap.example.org:143}INBOX", "username", "password")
     or die("не удалось подключиться: " . imap_last_error());

$MC = imap_check($mbox);

// Получим обзор всех писем в INBOX
$result = imap_fetch_overview($mbox,"1:{$MC->Nmsgs}",0);
foreach ($result as $overview) {
    echo "#{$overview->msgno} ({$overview->date}) - From: {$overview->from}
    {$overview->subject}\n";
}
imap_close($mbox);
?>
```

### Дивіться також

-   [imap\_fetchheader()](function.imap-fetchheader.md) \- Отримує заголовок повідомлення
