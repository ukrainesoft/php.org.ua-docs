- [«Threaded](class.threaded.md)
- [Threaded::count »](threaded.count.md)

- [PHP Manual](index.md)
- [Threaded](class.threaded.md)
- обробка

# Threaded::chunk

(PECL pthreads \>= 2.0.0)

Threaded::chunk — Обробка

### Опис

public **Threaded::chunk**(int `$size`, bool `$preserve`): array

Отримує фрагмент таблиці властивостей об'єктів заданого розміру,
необхідності зберігаючи ключі.

### Список параметрів

`size`
Кількість елементів для отримання.

`preserve`
Зберігати ключі елементів за промовчанням false.

### Значення, що повертаються

Масив елементів із таблиці властивостей об'єктів.

### Приклади

**Приклад #1 Отримання фрагмента таблиці властивостей**

` <?php$safe = new Threaded();while (count($safe) < 10) {    $safe[] = count($safe);}var_dump($safe->chunk(5));?> `

Результат виконання цього прикладу:

array(5) {
[0]=>
int(0)
[1]=>
int(1)
[2]=>
int(2)
[3]=>
int(3)
[4]=>
int(4)
}
