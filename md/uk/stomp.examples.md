- [« Типи ресурсів](stomp.resources.md)
- [Функції Stomp »](ref.stomp.md)

- [PHP Manual](index.md)
- [Stomp](book.stomp.md)
- Приклади

# Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

` <?php$queue  = '/queue/foo';$msg   = 'bar';/* Підключення */try {    $stomp = new Stomp('tcp://localhost:61613' e) {    die('Помилка підключення: ' . $e->getMessage());}/* Відправка повідомлення в черга 'foo' */$stomp->send($queue, $msg); в черги 'foo' */$stomp->subscribe($queue);/* Читання фрейму */$frame = $stomp->readFrame();if ($frame->body ====$msg) {     $frame); /* відповідь, що повідомлення було отримано */   $stomp->ack($frame);}/* Закриття з'єднання**/unset($stomp);?> `

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

` <?php$queue  = '/queue/foo';$msg   = 'bar';/* Підключення */$link = stomp_connect('ssl://localhost:61612');/* Перевірка підключення !$link) {    die('Помилка підключення: ' . stomp_connect_error());}/* Початок транзакції */stomp_begin($link, 't1');/* Відправка send , $queue, $msg, array('transaction' => 't1'));/* Виконання транзакції */stomp_commit($link, 't1');/* Підписка к повідомлень в'чері $link, $queue);/* Читання фрейму */$frame = stomp_read_frame($link);if ($frame['body'] === $msg) {   var_dump($frame); /* відгук, що повідомлення отримало */   stomp_ack($link, $frame['headers']['message-id']);}/* Закриття з'єднання */stomp_close($link);?> `

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
