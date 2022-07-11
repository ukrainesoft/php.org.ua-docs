- [« imap_subscribe](function.imap-subscribe.md)
- [imap_timeout »](function.imap-timeout.md)

- [PHP Manual](index.md)
- [Функції IMAP](ref.imap.md)
- Отримати дерево пов'язаних повідомлень

#imap_thread

(PHP 4 \>= 4.0.7, PHP 5, PHP 7, PHP 8)

imap_thread — Отримати дерево пов'язаних повідомлень

### Опис

**imap_thread**([IMAP\Connection](class.imap-connection.md) `$imap`,
int `$flags` = **`SE_FREE`**): array\|false

Повертає дерево пов'язаних повідомлень.

### Список параметрів

`imap`
Примірник [IMAP\Connection](class.imap-connection.md).

`flags`

### Значення, що повертаються

**imap_thread()** повертає асоціативний масив, що містить дерево
повідомлень, пов'язаних з допомогою `REFERENCES`, або **`false`** у разі
виникнення помилки.

Кожне повідомлення у поточній поштовій скриньці буде представлене як запис
у дереві в результуючому масиві:

- `$thread["XX.num"]` - номер поточного повідомлення

- `$thread["XX.next"]`

- `$thread["XX.branch"]`

### Список змін

| Версія | Опис |
| ------ | ---- |

### Приклади

**Приклад #1 Приклад використання **imap_thread()****

` <?php// Тут ми виводимо зв'язані повідомлення групи новостей в HTML$nntp = imap_open('{news.example.com:119/nntp}some.newsgroup', '', '');$ read nntp);foreach ($threads as $key => $val) {  $tree = explode('.', $key); if ($tree[1] == 'num') {   $header = imap_headerinfo($nntp, $val); echo "<ul>
<li>" . $header->fromaddress . "
";  } elseif ($tree[1] == 'branch') {    echo " </li>
</ul>
";  }}imap_close($nntp);?> `
