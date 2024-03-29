---
navigation:
  - stomp.hasframe.md: '« Stomp::hasFrame'
  - stomp.send.md: 'Stomp::send »'
  - index.md: PHP Manual
  - class.stomp.md: Stomp
title: 'Stomp::readFrame'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Stomp::readFrame

# stomp\_read\_frame

(PECL stomp >= 0.1.0)

Stomp::readFrame -- stomp\_read\_frame — Виконує операцію читання наступного кадру

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public Stomp::readFrame(string $class_name = "stompFrame"): stompframe
```

Процедурний стиль:

```methodsynopsis
stomp_read_frame(resource $link): array
```

Виконує операцію для читання наступного кадру. Якщо можливо, створює екземпляр зазначеного класу і передає параметри конструктору цього класу.

### Список параметрів

`link`

Тільки для процедурного стилю: ідентифікатор з'єднання stomp, отриманий з [stomp\_connect()](stomp.construct.md)

`class_name`

Назва класу для створення екземпляра. Якщо не вказано, повертається об'єкт stompFrame.

### Значення, що повертаються

> **Зауваження** :
> 
> Також може бути зазначений заголовок транзакції, що означає, що прийом повідомлення повинен бути частиною іменованої транзакції.

### список змін

| Версия | Опис |
| --- | --- |
| Stomp 0.4.0 | Добавлен параметр`class_name` |

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php

/* подключение */
try {
    $stomp = new Stomp('tcp://localhost:61613');
} catch(StompException $e) {
    die('Ошибка соединения: ' . $e->getMessage());
}

/* подписка на сообщения из очереди 'foo' */
$stomp->subscribe('/queue/foo');

/* чтение фрейма */
var_dump($stomp->readFrame());

/* закрытие подключения */
unset($stomp);

?>
```

Висновок наведеного прикладу буде схожим на:

```
object(StompFrame)#2 (3) {
  ["command"]=>
  string(7) "MESSAGE"
  ["headers"]=>
  array(5) {
    ["message-id"]=>
    string(41) "ID:php.net-55293-1257226743606-4:2:-1:1:1"
    ["destination"]=>
    string(10) "/queue/foo"
    ["timestamp"]=>
    string(13) "1257226805828"
    ["expires"]=>
    string(1) "0"
    ["priority"]=>
    string(1) "0"
  }
  ["body"]=>
  string(3) "bar"
}
```

**Приклад #2 Процедурний стиль**

```php
<?php

/* подключение */
$link = stomp_connect('ssl://localhost:61612');

/* проверка соединения */
if (!$link) {
    die('Ошибка соединения: ' . stomp_connect_error());
}

/* подписка на сообщения из очереди 'foo' */
stomp_subscribe($link, '/queue/foo');

/* чтение фрейма */
$frame = stomp_read_frame($link);

/* закрытие подключения */
stomp_close($link);

?>
```

Висновок наведеного прикладу буде схожим на:

```
array(3) {
  ["command"]=>
  string(7) "MESSAGE"
  ["body"]=>
  string(3) "bar"
  ["headers"]=>
  array(6) {
    ["transaction"]=>
    string(2) "t1"
    ["message-id"]=>
    string(41) "ID:php.net-55293-1257226743606-4:3:-1:1:1"
    ["destination"]=>
    string(10) "/queue/foo"
    ["timestamp"]=>
    string(13) "1257227037059"
    ["expires"]=>
    string(1) "0"
    ["priority"]=>
    string(1) "0"
  }
}
```
