- [«Stomp::hasFrame](stomp.hasframe.md)
- [Stomp::send »](stomp.send.md)

- [PHP Manual](index.md)
- [Stomp](class.stomp.md)
- Виконує операцію читання наступного кадру

# Stomp::readFrame

#stomp_read_frame

(PECL stomp \>= 0.1.0)

Stomp::readFrame - stomp_read_frame - Виконує операцію читання
наступного кадру

### Опис

Об'єктно-орієнтований стиль (метод):

public **Stomp::readFrame**(string `$class_name` = "stompFrame"):
[stompframe](class.stompframe.md)

Процедурний стиль:

**stomp_read_frame**(resource `$link`): array

Виконує операцію для читання наступного кадру. Якщо можливо, то створює
екземпляр зазначеного класу та передає параметри конструктору цього
класу.

### Список параметрів

`link`
Тільки для процедурного стилю: ідентифікатор з'єднання stomp,
отриманий із [stomp_connect()](stomp.construct.md).

`class_name`
Назва класу для створення екземпляра. Якщо не вказано, повертається об'єкт
stompFrame.

### Значення, що повертаються

> **Примітка**:
>
> Також може бути зазначений заголовок транзакції, що означає, що прийом
> повідомлення має бути частиною іменованої транзакції.

### Список змін

| Версія      | Опис                         |
|-------------|------------------------------|
| Stomp 0,4.0 | Доданий параметр class_name. |

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

`<?php/* підключення */try {    $stomp = new Stomp('tcp://localhost:61613');} catch(StompException $e) {    die('Помилка$>|| ));}/* підписка на повідомлення з черги 'foo' */$stomp->subscribe('/queue/foo');/* читання фрейму */var_dump($stomp->readFrame());/* закриття підключення */unset($stomp);?> `

Результатом виконання цього прикладу буде щось подібне:

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

**Приклад #2 Процедурний стиль**

` <?php/* підключення */$link = stomp_connect('ssl://localhost:61612');/* перевірка з'єднання */if (!$link) {    die('Помилка з'єднання: ' . . . . ;}/* підписка на повідомлення з черги 'foo' */stomp_subscribe($link, '/queue/foo');/* читання фрейму */$frame = stomp_read_frame($link);/* $link);?> `

Результатом виконання цього прикладу буде щось подібне:

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
