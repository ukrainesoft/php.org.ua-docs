- [« Threaded::chunk](threaded.chunk.md)
- [Threaded::extend »](threaded.extend.md)

- [PHP Manual](index.md)
- [Threaded](class.threaded.md)
- обробка

# Threaded::count

(PECL pthreads \>= 2.0.0)

Threaded::count — Обробка

### Опис

public **Threaded::count**(): int

Повертає кількість властивостей цього об'єкта.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

### Приклади

**Приклад #1 Підрахунок властивостей об'єкта**

` <?php$safe = new Threaded();while (count($safe) < 10) {    $safe[] = count($safe);}var_dump(count($safe));?> `

Результат виконання цього прикладу:

int(10)
