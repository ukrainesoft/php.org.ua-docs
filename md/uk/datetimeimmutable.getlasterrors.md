- [« DateTimeImmutable::createFromMutable](datetimeimmutable.createfrommutable.md)
- [DateTimeImmutable::modify »](datetimeimmutable.modify.md)

- [PHP Manual](index.md)
- [DateTimeImmutable](class.datetimeimmutable.md)
- Повертає попередження та помилки

# DateTimeImmutable::getLastErrors

(PHP 5 \>= 5.5.0, PHP 7, PHP 8)

DateTimeImmutable::getLastErrors — Повертає попередження та помилки

### Опис

public static **DateTimeImmutable::getLastErrors**(): array\|false

Повертає масив, що містить повідомлення про помилки та попередження,
виявлені при розборі рядка дати/часу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив, що містить інформацію про попередження та помилки або
**`false`**, якщо немає ні попереджень, ні помилок.

### Приклади

**Приклад #1 Приклад використання
**DateTimeImmutable::getLastErrors()****

Об'єктно-орієнтований стиль

` <?phptry {    $date = new DateTimeImmutable('asdfasdf');} catch (Exception $e) {    // Тільки в метах демонстрації... | // в об'єктно-орієнтованому стилі краще робити так:    // echo $e->getMessage();}?> `

Результат виконання даних прикладів:

Array
(
[warning_count] => 1
[warnings] => Array
(
[6] => Double timezone specification
)

[error_count] => 1
[errors] => Array
(
[0] => The timezone не може бути зроблено в 데이터베이스
)

)

Індекси 6 та 0 вказують на символьні позиції у рядку, де відбулася
помилка.
