---
navigation:
  - phar.converttoexecutable.html: '« Phar::convertToExecutable'
  - phar.count.html: 'Phar::count »'
  - index.html: PHP Manual
  - class.phar.html: Phar
title: 'Phar::copy'
---
# Phar::copy

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

Phar::copy — Копіює один файл усередині phar-архіву в інший новий файл усередині phar-архіву

### Опис

```methodsynopsis
public Phar::copy(string $from, string $to): bool
```

> **Зауваження**
> 
> Для коректної роботи з об'єктами [Phar](class.phar.html) цьому методу необхідне встановлення значення php.ini `phar.readonly` в `0`. В іншому випадку, буде викинуто виняток [PharException](class.pharexception.md)

Копіює внутрішній файл phar-архіву в інший новий файл усередині phar-архіву. Це об'єктно-орієнтована альтернатива використанню [copy()](function.copy.md) з обгорткою потоку phar.

### Список параметрів

`from`

`to`

### Значення, що повертаються

повертає **`true`** у разі успішного виконання, але безпечніше укласти виклик методу в блок try/catch і вважати його успішним, якщо не було викинуто виняток.

### Помилки

Викидає виняток [UnexpectedValueException](class.unexpectedvalueexception.html) якщо: вихідний файл не існує, цільовий файл вже існує, доступ на запис вимкнено, відкриття будь-якого файлу неможливе або читання вихідного файлу зазнало невдачі. Якщо запис змін до phar не вдався, буде викинуто виняток [PharException](class.pharexception.md)

### Приклади

**Приклад #1 Приклад використання **Phar::copy()****

У цьому прикладі показано використання методу **Phar::copy()** і еквівалентної йому за функціональністю обгортки потоку для вирішення однієї і тієї ж задачі. Основною відмінністю між цими двома підходами є обробка помилок. Усі методи Phar викидають винятки, тоді як обгортка потоку використовує [triggererror()](function.trigger-error.md)

```php
<?php
try {
    $phar = new Phar('myphar.phar');
    $phar['a'] = 'привет';
    $phar->copy('a', 'b');
    echo $phar['b']; // будет выведено "привет"
} catch (Exception $e) {
    // обработка ошибок
}

// обёртка потока, эквивалентная коду выше.
// в случае возникновения ошибки будет вызвано предупреждение E_WARNING, а не исключение
copy('phar://myphar.phar/a', 'phar//myphar.phar/c');
echo file_get_contents('phar://myphar.phar/c'); // будет выведено "привет"
?>
```
