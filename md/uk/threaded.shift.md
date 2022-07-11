- [« Threaded::run](threaded.run.md)
- [Threaded::synchronized »](threaded.synchronized.md)

- [PHP Manual](index.md)
- [Threaded](class.threaded.md)
- обробка

# Threaded::shift

(PECL pthreads \>= 2.0.0)

Threaded::shift — Обробка

### Опис

public **Threaded::shift**():
[mixed](language.types.declarations.md#language.types.declarations.mixed)

Переміщує елемент із таблиці властивостей об'єкта.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перший елемент таблиці властивостей об'єкта.

### Приклади

**Приклад #1 Переміщення першого елемента з таблиці властивостей пов'язаного
об'єкта**

` <?php$safe = new Threaded();while (count($safe) < 10)   $safe[] = count($safe);var_dump($safe->shift());?> `

Результат виконання цього прикладу:

int(0)
