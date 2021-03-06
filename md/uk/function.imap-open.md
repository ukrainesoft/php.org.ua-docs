- [« imap_num_recent](function.imap-num-recent.md)
- [imap_ping»](function.imap-ping.md)

- [PHP Manual](index.md)
- [Функції IMAP](ref.imap.md)
- Відкриває потік IMAP до поштової скриньки

#imap_open

(PHP 4, PHP 5, PHP 7, PHP 8)

imap_open — Відкриває потік IMAP до поштової скриньки

### Опис

**imap_open**(
string `$mailbox`,
string `$user`,
string `$password`,
int `$flags` = 0,
int `$retries` = 0,
array `$options` = [] ): [IMAP\Connection](class.imap-connection.md)\|false

Відкриває потік IMAP до mailbox.

Ця функція також може використовуватися для відкриття потоку до серверів
POP3 і NNTP, але частина функцій та особливостей буде працювати тільки з
серверами IMAP.

### Список параметрів

`mailbox`
Ім'я поштової скриньки складається із сервера та шляху до поштової скриньки на ньому.
Спеціальне ім'я `INBOX` використовується для поштової скриньки поточного
користувача. Імена поштових скриньок, що містять міжнародні
символи крім входять у друкований простір ASCII, мають бути
закодовані за допомогою
[imap_utf7_encode()](function.imap-utf7-encode.md).

**Увага**
Якщо
[imap.enable_insecure_rsh](imap.configuration.md#ini.imap.enable-insecure-rsh)
не вимкнено, то передача в цей параметр не перевірених даних *не
безпечна*.

Серверна частина, укладена у фігурні дужки '{' і '}', складається з
імені або IP-адреси сервера, опціонального порту (попереднього
двокрапкою) та опціональних специфікацій протоколу (попереджених слідом)
'/').

Серверна частина є обов'язковою у всіх параметрах поштового
ящика.

Всі імена, що починаються з `{` є віддаленими іменами і мають такий
синтаксис
`"{" remote_system_name [":" port] [flags] "}" [mailbox_name]`
де:

- `remote_system_name` - повне доменне ім'я сервера, або IP-адреса в
квадратних дужках.
- `port` - необов'язковий параметр. Визначає порт сервера
- `flags` - опціональні прапори, дивись таблицю нижче
- `mailbox_name` - ім'я поштової скриньки. Типово INBOX

| Підкреслити                                  | Опис                                                                                                                                    |
| -------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| /service=*service*                           | сервіс доступу до поштової скриньки. Типово "imap"                                                                                      |                                                                                                                                         
| /user=*user*                                 | Ім'я користувача для входу на сервер                                                                                                    |
| /authuser=*user*                             | віддалений користувач для автентифікації; якщо зазначено, це буде той користувач, чий пароль використовується (наприклад administrator) |
| /anonymous                                   | віддалений доступ під анонімним користувачем                                                                                            |
| /debug                                       | записувати телеметрію протоколу до спеціального лог-файлу програми                                                                      |
| /secure                                      | не передавати пароль через мережу у вигляді нешифрованого тексту                                                                        |
| /imap, /imap2, /imap2bis, /imap4, /imap4rev1 | еквівалентно /service=imap                                                                                                              |
| /pop3                                        | еквівалентно /service=pop3                                                                                                              |
| /nntp                                        | еквівалентно /service=nntp                                                                                                              |
| '/norsh'                                     | не використовувати rsh чи ssh для встановлення переавторизованої сесії IMAP                                                             |
| /ssl                                         | використовувати SSL для шифрування сесії                                                                                                |
| /validate-cert                               | перевіряти сертифікати серверів TLS/SSL (стандартна поведінка)                                                                          |
| /novalidate-cert                             | не перевіряти сертифікати від серверів TLS/SSL. корисно для серверів із самопідписаним сертифікатом                                     |
| /tls                                         | примусово використовувати start-TLS для шифрування сесії та відкидати з'єднання з серверами, що його не підтримують                     |
| /notls                                       | не застосовувати start-TLS для шифрування сесії, навіть якщо сервер підтримує                                                           |
| '/readonly'                                  | запит відкриття в режимі "тільки читання" (тільки IMAP; ігнорується для NNTP та видає помилку для SMTP та POP3)                         |

**Опціональні прапори**

`user`
Ім'я користувача

`password`
Пароль користувача `user`

`flags`
`flags` - бітова маска з однієї або кількох констант:

- **`OP_READONLY`** - відкрити поштову скриньку тільки для читання
- **`OP_ANONYMOUS`** - не використовувати та не оновлювати `.newsrc` для
новин (тільки NNTP)
- **`OP_HALFOPEN`** - відкрити з'єднання, але не підключатися до
поштову скриньку для ім'я IMAP та NNTP.
- **`CL_EXPUNGE`** - автоматично видаляти всі позначені для
видалення повідомлення при закритті поштової скриньки (див.
[imap_delete()](function.imap-delete.md) та
[imap_expunge()](function.imap-expunge.md))
- **`OP_DEBUG`** - домовленості щодо протоколу налагодження
- **`OP_SHORTCACHE`** - коротке кешування (тільки `elt`)
- **`OP_SILENT`** - не передавати події (внутрішнє використання)
- **`OP_PROTOTYPE`** - повернути прототип драйвера
- **`OP_SECURE`** - не здійснювати безпечну автентифікацію

`retries`
Максимальна кількість спроб з'єднання

`options`
Параметри для підключення. Для встановлення одного або кількох параметрів
з'єднання можна використовувати такі (рядки) ключі:

- `DISABLE_AUTHENTICATOR` - забороняє властивості автентифікації

### Значення, що повертаються

У разі успішного виконання повертає екземпляр
[IMAP\Connection](class.imap-connection.md) або **`false`** у випадку
виникнення помилки.

### Список змін

| Версія | Опис                                                                                                                               |
| ------ | ---------------------------------------------------------------------------------------------------------------------------------- |
| 8.1.0  | Повертає екземпляр [IMAP\Connection](class.imap-connection.md); раніше повертався ресурс ([resource](language.types.resource.md)). |

### Приклади

**Приклад #1 Різні способи використання **imap_open()****

`<?php// Для підключення к серверу IMAP, працюючому на порту 143 на локальній машині, зробити наступне:$mbox = imap_open("{localhost:143}INBOX" до серверу POP3, працюючому на порту 110 на локальній машині, використовувати:$mbox = imap_open ("{localhost:110/pop3}INBOX", "user_id", P   додати /ssl після протоколу// specification:$mbox = imap_open ("{localhost:993/imap/ssl}INBOX", "user_id", "password");// Для підключення к серверу // додати /ssl/novalidate-cert після специфікації протоколу:$mbox = imap_open ("{localhost:995/pop3/ssl/novalidate-cert}", "user_id", "password");// Д| , працюючому на порту 119 на локальній машині, використовувати:$nntp = imap_open ("{localhost:119/nntp}comp.test", "", ""); або// IP-адреса сервера, до якого ви хочете п відключитися.?> `

**Приклад #2 Приклад використання **imap_open()****

` <?php$mbox = imap_open("{imap.example.org:143}", "username", "password");echo "<h1>Поштові ящики</h1>
";$folders = imap_listmailbox($mbox, "{imap.example.org:143}", "*");if ($folders == false) {    echo "Невдалий  виклик<br />
";} else {    foreach ($folders as $val) {       echo $val . "<br />
";    }}echo "<h1>Заголовки в INBOX</h1>
";$headers = imap_headers($mbox);if ($headers == false) {    echo "Невдалий виклик<br />
";} else {    foreach ($headers as $val) {       echo $val . "<br />
";   }}imap_close($mbox);?> `

### Дивіться також

- [imap_close()](function.imap-close.md) - Закрити потік IMAP
