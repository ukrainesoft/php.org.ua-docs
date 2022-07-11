- [«Stomp::send](stomp.send.md)
- [Stomp::subscribe »](stomp.subscribe.md)

- [PHP Manual](index.md)
- [Stomp](class.stomp.md)
- Встановлює граничний час очікування операції читання

# Stomp::setReadTimeout

#stomp_set_read_timeout

(PECL stomp \>= 0.3.0)

Stomp::setReadTimeout -- stomp_set_read_timeout -- Встановлює
граничний час очікування операції читання

### Опис

Об'єктно-орієнтований стиль (метод):

public **Stomp::setReadTimeout**(int `$seconds`, int `$microseconds` =
?): void

Процедурний стиль:

**stomp_set_read_timeout**(resource `$link`, int `$seconds`, int
`$microseconds` = ?): void

Встановлює граничний час очікування операції читання.

### Список параметрів

`link`
Тільки для процедурного стилю: ідентифікатор з'єднання stomp,
отриманий із [stomp_connect()](stomp.construct.md).

`seconds`
Секундна частина часу очікування операції.

`microseconds`
Мікросекундний час очікування операції.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

`<?php/* підключення */try {    $stomp = new Stomp('tcp://localhost:61613');} catch(StompException $e) {    die('Помилка$>|| ));}$stomp->setReadTimeout(10);/* закриття підключення */unset($stomp);?> `

**Приклад #2 Процедурний стиль**

` <?php/* підключення */$link = stomp_connect('ssl://localhost:61612');/* перевірка з'єднання */if (!$link) {    die('Помилка підключення: ' . . . . ;}stomp_set_read_timeout($link, 10);/* закриття підключення */stomp_close($link);?> `
