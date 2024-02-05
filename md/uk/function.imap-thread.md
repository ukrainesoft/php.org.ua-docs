---
navigation:
  - function.imap-subscribe.md: « imap\_subscribe
  - function.imap-timeout.md: imap\_timeout »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_thread
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_thread

(PHP 4 >= 4.0.7, PHP 5, PHP 7, PHP 8)

imap\_thread — Отримує дерево пов'язаних повідомлень

### Опис

```methodsynopsis
imap_thread(IMAP\Connection $imap, int $flags = SE_FREE): array|false
```

Повертає дерево пов'язаних повідомлень.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`flags`

### Значення, що повертаються

**imap\_thread()** повертає асоціативний масив, що містить дерево повідомлень, пов'язаних за допомогою `REFERENCES`, или\*\*`false`\*\*в случае возникновения ошибки.

Кожне повідомлення у поточній поштовій скриньці буде представлене як запис у дереві в результуючому масиві:

-   $thread\["XX.num"\]- Номер поточного повідомлення
    
-   $thread\["XX.next"\]
    
-   $thread\["XX.branch"\]
    

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Приклади

**Приклад #1 Приклад використання** imap\_thread()\*\*\*\*

```php
<?php

// Здесь мы выводим связанные сообщения группы новостей в HTML

$nntp = imap_open('{news.example.com:119/nntp}some.newsgroup', '', '');
$threads = imap_thread($nntp);

foreach ($threads as $key => $val) {
  $tree = explode('.', $key);
  if ($tree[1] == 'num') {
    $header = imap_headerinfo($nntp, $val);
    echo "<ul>\n\t<li>" . $header->fromaddress . "\n";
  } elseif ($tree[1] == 'branch') {
    echo "\t</li>\n</ul>\n";
  }
}

imap_close($nntp);

?>
```
