Отримати дерево пов'язаних повідомлень

-   [« imap\_subscribe](function.imap-subscribe.html)
    
-   [imap\_timeout »](function.imap-timeout.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Отримати дерево пов'язаних повідомлень
    

# imapthread

(PHP 4> = 4.0.7, PHP 5, PHP 7, PHP 8)

imapthread — Отримати дерево пов'язаних повідомлень

### Опис

```methodsynopsis
imap_thread(IMAP\Connection $imap, int $flags = SE_FREE): array|false
```

Повертає дерево пов'язаних повідомлень.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.html)

`flags`

### Значення, що повертаються

**imapthread()** повертає асоціативний масив, що містить дерево повідомлень, пов'язаних за допомогою `REFERENCES`, або **`false`** у разі виникнення помилки.

Кожне повідомлення у поточній поштовій скриньці буде представлене як запис у дереві в результуючому масиві:

-   $thread"XX.num" - Номер поточного повідомлення
    
-   $thread"ХХ.некст"
    
-   $thread"XX.branch"
    

### список змін

| Версия | Описание                                                                                                                                                 |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **imapthread()****

```php
<?php

// Здесь мы выводим связанные сообщения группы новостей в HTML

$nntp = imap_open('{news.example.com:119/nntp}some.newsgroup', '', '');
$threads = imap_thread($nntp);

foreach ($threads as $key => $val) {
  $tree = explode('.', $key);
  if ($tree[1] == 'num') {
    $header = imap_headerinfo($nntp, $val);
    echo "<ul>\n\t<li>" . $header->fromaddress . "\n";
  } elseif ($tree[1] == 'branch') {
    echo "\t</li>\n</ul>\n";
  }
}

imap_close($nntp);

?>
```