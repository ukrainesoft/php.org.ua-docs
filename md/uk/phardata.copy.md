---
navigation:
  - phardata.converttoexecutable.md: '« PharData::convertToExecutable'
  - phardata.decompress.md: 'PharData::decompress »'
  - index.md: PHP Manual
  - class.phardata.md: PharData
title: 'PharData::copy'
---
# PharData::copy

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::copy — Скопіювати файл із tar/zip-архіву в новий файл усередині нього ж

### Опис

```methodsynopsis
public PharData::copy(string $from, string $to): bool
```

Копіює файл з tar/zip-архіву в новий файл усередині нього. Це об'єктно-орієнтована альтернатива для [copy()](function.copy.md) з потоковою обгорткою phar.

### Список параметрів

`from`

`to`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання. Але краще використовувати механізм перехоплення винятків контролю успішності.

### Помилки

Викидає виняток [UnexpectedValueException](class.unexpectedvalueexception.md), якщо файл, що копіюється, відсутній, новий файл вже існує, запис заборонено або виникли проблеми з відкриттям читанням вихідного файлу. У разі проблем із записом на диск кидається виняток [PharException](class.pharexception.md)

### Приклади

**Приклад #1 Приклад використання **PharData::copy()****

У прикладі показано використання **PharData::copy()** та аналог з використанням потокової обгортки. Головна різниця між цими підходами – обробка помилок. Усі методи PharData викидають винятки, тоді як потокові обгортки використовують функцію [triggererror()](function.trigger-error.md)

```php
<?php
try {
    $phar = new PharData('myphar.tar');
    $phar['a'] = 'hi';
    $phar->copy('a', 'b');
    echo $phar['b']; // выводит "phar://myphar.tar/b"
} catch (Exception $e) {
    // Обработка ошибок
}

// Аналог с использованием потоковых обёрток.
// В случае проблем вместо исключения вызывается ошибка уровня E_WARNINGS
copy('phar://myphar.tar/a', 'phar//myphar.tar/c');
echo file_get_contents('phar://myphar.tar/c'); // выводит "hi"
?>
```
