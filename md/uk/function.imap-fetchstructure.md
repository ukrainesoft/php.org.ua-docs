---
navigation:
  - function.imap-fetchmime.md: « imap\_fetchmime
  - function.imap-fetchtext.md: imap\_fetchtext »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_fetchstructure
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_fetchstructure

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_fetchstructure — Читає структуру вказаного повідомлення

### Опис

```methodsynopsis
imap_fetchstructure(IMAP\Connection $imap, int $message_num, int $flags = 0): stdClass|false
```

Витягує інформацію про структуру вказаного повідомлення.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`message_num`

Номер повідомлення

`flags`

Якщо поставлено як **`FT_UID`**, то в`message_num` повинні бути `UID` повідомлень, а не їхні номери.

### Значення, що повертаються

Повертає об'єкт із властивостями, переліченими в таблиці нижче або \*\*`false`\*\*в случае возникновения ошибки.

< td>id< td>Масив об'єктів, кожен з яких має властивості `"attribute"` та `"value"`, що відповідають параметрам `Content-disposition` заголовка MIME.

<table class="doctable table"><caption><strong>Об'єкт, що повертається <span class="function"><strong>imap_fetchstructure()</strong></span></strong></caption><tbody class="tbody"><tr><td>type</td><td>Первинний тип тіла</td></tr><tr><td>encoding</td><td>Кодування тіла</td></tr><tr><td>ifsubtype</td><td><strong><code>true</code></strong>, якщо є рядок підтипу</td></tr><tr><td>subtype</td><td><abbr title="Multipurpose Internet Mail Extensions">MIME</abbr>-підтип</td></tr><tr><td>ifdescription</td><td><strong><code>true</code></strong>, якщо є рядок опису</td></tr><tr><td>description</td><td>Контент рядка опису</td></tr><tr><td>ifid</td><td><strong><code>true</code></strong>, якщо є ідентифікатор рядка</td></tr><tr><td>Рядок ідентифікатор</td></tr><tr><td>lines</td><td>Кількість рядків</td></tr><tr><td>bytes</td><td>Кількість байт</td></tr><tr><td>ifdisposition</td><td><strong><code>true</code></strong>, якщо є Рядок розташування</td></tr><tr><td>disposition</td><td>Рядок розташування</td></tr><tr><td>ifdparameters</td><td><strong><code>true</code></strong>, якщо є масив <var class="varname">dparameters</var></td></tr><tr><td>dparameters</td></tr><tr><td>ifparameters</td><td>&lt; strong&gt;<code>true</code>, якщо є масив параметрів</td></tr><tr><td>parameters</td><td>Масив об'єктів, кожен з яких має властивості &lt; code class="literal"&gt;"attribute" та <code class="literal">"value"</code>.</td></tr><tr><td>parts</td><td>Масив об'єктів ідентичних за структурою з верхньорівневим об'єктом, кожен з яких відповідає <abbr title="Multipurpose Internet Mail Extensions">MIME</abbr> частини тіла.</td></tr></tbody></table>

**Первинний тип тіла (значення можуть відрізнятися залежно від бібліотеки, що використовується, так що рекомендується використовувати константи)**

| Значение | Тип | Константа |
| --- | --- | --- |
|  | text | TYPETEXT |
|  | multipart | TYPEMULTIPART |
|  | message | TYPEMESSAGE |
| 3 | application | TYPEAPPLICATION |
| 4 | audio | TYPEAUDIO |
| 5 | image | TYPEIMAGE |
| 6 | video | TYPEVIDEO |
| 7 | model | TYPEMODEL |
| 8 | other | TYPEOTHER |

**Кодування (значення можуть відрізнятися в залежності від бібліотеки, що використовується, так що рекомендується використовувати константи)**

| Значение | Тип | Константа |
| --- | --- | --- |
|  | 7bit | ENC7BIT |
|  | 8bit | ENC8BIT |
|  | Binary | ENCBINARY |
| 3 | Base64 | ENCBASE64 |
| 4 | Quoted-Printable | ENCQUOTEDPRINTABLE |
| 5 | other | ENCOTHER |

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Дивіться також

-   [imap\_fetchbody()](function.imap-fetchbody.md) \- Витягує конкретну секцію тіла повідомлення
-   [imap\_bodystruct()](function.imap-bodystruct.md) \- Читає структуру вказаної секції тіла заданого повідомлення
