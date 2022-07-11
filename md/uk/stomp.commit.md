- [« Stomp::begin](stomp.begin.md)
- [Stomp::\_\_construct »](stomp.construct.md)

- [PHP Manual](index.md)
- [Stomp](class.stomp.md)
- Виконує поточну транзакцію

# Stomp::commit

#stomp_commit

(PECL stomp \>= 0.1.0)

Stomp::commit -- stomp_commit — Виконує поточну транзакцію

### Опис

Об'єктно-орієнтований стиль (метод):

public **Stomp::commit**(string `$transaction_id`, array `$headers` =
?): bool

Процедурний стиль:

**stomp_commit**(resource `$link`, string `$transaction_id`, array
`$headers` = ?): bool

Виконує поточну транзакцію.

### Список параметрів

`link`
Тільки для процедурного стилю: ідентифікатор з'єднання stomp,
отриманий із [stomp_connect()](stomp.construct.md).

`transaction_id`
Ідентифікатор транзакції.

`headers`
Асоціативний масив, що містить додаткові заголовки (приклад:
receipt).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

`<?php/* підключення */try {    $stomp = new Stomp('tcp://localhost:61613');} catch(StompException $e) {    die('Помилка$>|| ));}/* Початок транзакції */$stomp->begin('t1');/* відправлення повідомлення в черга */$stomp->send('/queue/foo', 'bar', array('transaction ' => 't1'));/* виконання транзакції */$stomp->commit('t1');/* закриття підключення */unset($stomp);?> `

**Приклад #2 Процедурний стиль**

` <?php/* підключення */$link = stomp_connect('tcp://localhost:61613');/* перевірка підключення */if (!$link) {    die('Помилка з'єднання: ' . . . . ;}/* Початок транзакції */stomp_begin($link, 't1');/* Відправлення повідомлення в черга 'foo' */stomp_send($link, '/queue/foo', 'bar', arra => 't1'));/* Виконання транзакції */stomp_commit($link, 't1');/* Закриття зміни */stomp_close($link);?> `

### Примітки

**Підказка**

Stomp асинхронний за своєю суттю. Синхронний зв'язок може бути реалізований
додаванням receipt-заголовка. Це змусить методи нічого не повертати,
доки сервер не підтвердить отримання повідомлення або не буде перевищено
час очікування повідомлення.
