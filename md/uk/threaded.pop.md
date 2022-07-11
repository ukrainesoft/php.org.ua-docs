- [« Threaded::notifyOne](threaded.notifyone.md)
- [Threaded::run »](threaded.run.md)

- [PHP Manual](index.md)
- [Threaded](class.threaded.md)
- обробка

# Threaded::pop

(PECL pthreads \>= 2.0.0)

Threaded::pop — Обробка

### Опис

public **Threaded::pop**(): bool

Витягує елемент із таблиці властивостей об'єкта.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Останній елемент таблиці властивостей об'єктів.

### Приклади

**Приклад #1 Вилучення останнього елемента з таблиці властивостей пов'язаного
об'єкта**

` <?php$safe = new Threaded();while (count($safe) < 10)   $safe[] = count($safe);var_dump($safe->pop());?> `

Результат виконання цього прикладу:

int(9)
