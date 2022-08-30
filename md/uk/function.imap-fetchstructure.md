Прочитати структуру вказаного повідомлення

-   [« imapfetchmime](function.imap-fetchmime.html)
    
-   [imapfetchtext »](function.imap-fetchtext.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Прочитати структуру вказаного повідомлення
    

# imapfetchstructure

(PHP 4, PHP 5, PHP 7, PHP 8)

imapfetchstructure — Прочитати структуру вказаного повідомлення

### Опис

```methodsynopsis
imap_fetchstructure(IMAP\Connection $imap, int $message_num, int $flags = 0): stdClass|false
```

Витягує інформацію про структуру вказаного повідомлення.

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.html)

`message_num`

Номер повідомлення

`flags`

Якщо поставлено як **`FT_UID`**, то в `message_num` повинні бути `UID` повідомлень, а не їхні номери.

### Значення, що повертаються

Повертає об'єкт із властивостями, переліченими в таблиці нижче або **`false`** у разі виникнення помилки.

< td>id

<table class="doctable table"><caption><strong>Об'єкт, що повертається <span class="function"><strong>imap_fetchstructure()</strong></span></strong></caption><tbody class="tbody"><tr><td>type</td><td>Первинний тип тіла</td></tr><tr><td>encoding</td><td>Кодування тіла</td></tr><tr><td>ifsubtype</td><td><strong><code>true</code></strong>, якщо є рядок підтипу</td></tr><tr><td>subtype</td><td><abbr title="Multipurpose Internet Mail Extensions">MIME</abbr>-підтип</td></tr><tr><td>ifdescription</td><td><strong><code>true</code></strong>, якщо є рядок опису</td></tr><tr><td>description</td><td>Контент рядка опису</td></tr><tr><td>ifid</td><td><strong><code>true</code></strong>, якщо є ідентифікатор рядка</td></tr><tr><td>Рядок ідентифікатор</td></tr><tr><td>lines</td><td>Кількість рядків</td></tr><tr><td>bytes</td><td>Кількість байт</td></tr><tr><td>ifdisposition</td><td><strong><code>true</code></strong>, якщо є рядок розташування</td></tr><tr><td>dispositio n</td><td>Рядок розташування</td></tr><tr><td>ifdparameters</td><td><strong><code>true</code></strong>, якщо є масив <var class="varname">dparameters</var></td></tr><tr><td>dparameters</td><td>Масив об'єктів, кожен з яких має властивості <code class="literal ">"attribute"</code> та <code class="literal">"value"</code>, що відповідають параметрам <code class="literal">Content-disposition</code> заголовка <abbr title="Multipurpose Internet Mail Extensions">MIME</abbr>.</td></tr><tr><td>ifparameters</td><td><strong><code>true</code></strong>, якщо є масив параметрів</td></tr><tr><td>parameters</td><td>Масив об'єктів, кожен з яких має властивості <code class="literal">"attribute"</code> та &lt; code class="literal"&gt;"value".</td></tr><tr><td>parts</td><td>Масив об'єктів ідентичних за структурою з верхньорівневим об'єктом, кожен з яких відповідає <abbr title="Multipurpose Internet Mail Extensions">MIME</abbr> частини тіла.</td></tr></tbody></table>

**Первинний тип тіла (значення можуть відрізнятися залежно від бібліотеки, що використовується, так що рекомендується використовувати константи)**

| Значение | Тип | Константа |
| --- | --- | --- |
|  | text | TYPETEXT |
|  | multipart | TYPEMULTIPART |
|  | message | TYPEMESSAGE |
|  | application | TYPEAPPLICATION |
|  | audio | TYPEAUDIO |
|  | image | TYPEIMAGE |
|  | video | TYPEVIDEO |
|  | model | TYPEMODEL |
|  | other | TYPEOTHER |

**Кодування (значення можуть відрізнятися залежно від бібліотеки, що використовується, так що рекомендується використовувати константи)**

| Значение | Тип | Константа |
| --- | --- | --- |
|  | 7bit | ENC7BIT |
|  | 8bit | ENC8BIT |
|  | Binary | ENCBINARY |
|  | Base64 | ENCBASE64 |
|  | Quoted-Printable | ENCQUOTEDPRINTABLE |
|  | other | ENCOTHER |

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [imapfetchbody()](function.imap-fetchbody.html) - Витягти конкретну секцію тіла повідомлення
-   [imapbodystruct()](function.imap-bodystruct.html) - Прочитати структуру вказаної секції тіла заданого повідомлення