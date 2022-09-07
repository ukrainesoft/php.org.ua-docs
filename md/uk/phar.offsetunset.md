---
navigation:
  - phar.offsetset.md: '« Phar::offsetSet'
  - phar.running.md: 'Phar::running »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::offsetUnset'
---
# Phar::offsetUnset

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

Phar::offsetUnset — Видалити файл із phar-архіву

### Опис

```methodsynopsis
public Phar::offsetUnset(string $localName): void
```

> **Зауваження**
> 
> Для коректної роботи з об'єктами [Phar](class.phar.md) цьому методу необхідне встановлення значення php.ini `phar.readonly` в `0`. В іншому випадку, буде викинуто виняток [PharException](class.pharexception.md)

Це реалізація інтерфейсу [ArrayAccess](class.arrayaccess.md)дозволяє маніпулювати вмістом Phar-архіву в стилі доступу до елементів масиву. offsetUnset використовується для видалення файлів і запускається щоразу, коли використовується конструкція [unset()](function.unset.md)

### Список параметрів

`localName`

Назва файлу (відносний шлях).

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Якщо опція [phar.readonly](phar.configuration.md#ini.phar.readonly) встановлений в `1`, то буде викинуто виняток [BadMethodCallException](class.badmethodcallexception.md)Так як модифікувати Phar-архів можна тільки, якщо phar.readonly дорівнює `0`. Якщо виникнуть проблеми із записом на диск - викидається виняток [PharException](class.pharexception.md)

### Приклади

**Приклад #1 Приклад використання **Phar::offsetUnset()****

```php
<?php
$p = new Phar('/path/to/my.phar', 0, 'my.phar');
try {
    // удаляет file.txt из my.phar путём вызова offsetUnset
    unset($p['file.txt']);
} catch (Exception $e) {
    echo 'Не удалось удалить file.txt: ', $e;
}
?>
```

### Дивіться також

-   [Phar::offsetExists()](phar.offsetexists.md) - Визначити, чи є файл у архіві
-   [Phar::offsetGet()](phar.offsetget.md) - Отримати PharFileInfo об'єкт для конкретного файлу
-   [Phar::offsetSet()](phar.offsetset.md) - Зміна вмісту файлу
-   [Phar::unlinkArchive()](phar.unlinkarchive.md) - Повністю видалити архів з пам'яті та з диска
-   [Phar::delete()](phar.delete.md) - Видаляє файл усередині phar-архіву
