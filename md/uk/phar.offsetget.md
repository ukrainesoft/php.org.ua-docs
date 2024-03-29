---
navigation:
  - phar.offsetexists.md: '« Phar::offsetExists'
  - phar.offsetset.md: 'Phar::offsetSet »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::offsetGet'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Phar::offsetGet

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

Phar::offsetGet — Отримати об'єкт [PharFileInfo](class.pharfileinfo.md)для конкретного файла

### Опис

```methodsynopsis
public Phar::offsetGet(string $localName): SplFileInfo
```

Це реалізація інтерфейсу [ArrayAccess](class.arrayaccess.md), що дозволяє маніпулювати вмістом Phar-архіву в стилі доступу до елементів масиву . **Phar::offsetGet()** використовується для отримання файлів з архіву.

### Список параметрів

`localName`

Ім'я файлу (відносний шлях).

### Значення, що повертаються

Об'єкт класу [PharFileInfo](class.pharfileinfo.md). Можна використовувати для отримання інформації про файл та для отримання контенту через ітерування.

### Помилки

Викидає виняток [BadMethodCallException](class.badmethodcallexception.md)якщо такого файлу немає.

### Приклади

**Приклад #1 Приклад використання** Phar::offsetGet()\*\*\*\*

Як і для будь-якого іншого класу, що реалізує [ArrayAccess](class.arrayaccess.md), метод**Phar::offsetGet()** буде викликано автоматично під час використання оператора `[]`

```php
<?php
$p = new Phar(dirname(__FILE__) . '/myphar.phar', 0, 'myphar.phar');
$p['exists.txt'] = "file exists\n";
try {
    // автоматический вызов offsetGet()
    echo $p['exists.txt'];
    echo $p['doesnotexist.txt'];
} catch (BadMethodCallException $e) {
    echo $e;
}
?>
```

Результат виконання наведеного прикладу:

```
file exists
Entry doesnotexist.txt does not exist
```

### Дивіться також

-   [Phar::offsetExists()](phar.offsetexists.md) \- Визначити, чи є файл у архіві
-   [Phar::offsetSet()](phar.offsetset.md) \- Зміна вмісту файлу
-   [Phar::offsetUnset()](phar.offsetunset.md) \- Видалити файл із phar-архіву
