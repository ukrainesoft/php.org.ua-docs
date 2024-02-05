---
navigation:
  - phar.offsetget.md: '« Phar::offsetGet'
  - phar.offsetunset.md: 'Phar::offsetUnset »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::offsetSet'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Phar::offsetSet

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

Phar::offsetSet — Зміна вмісту файлу

### Опис

```methodsynopsis
public Phar::offsetSet(string $localName, resource|string $value): void
```

> **Зауваження** :
> 
> Для коректної роботи з об'єктами [Phar](class.phar.md) цьому методу необхідне встановлення значення php.ini `phar.readonly`в . В іншому випадку, буде викинуто виняток [PharException](class.pharexception.md)

Це реалізація інтерфейсу [ArrayAccess](class.arrayaccess.md)дозволяє маніпулювати вмістом Phar-архіву в стилі доступу до елементів масиву. offsetSet використовується для зміни контенту існуючого файлу або для створення нового.

### Список параметрів

`localName`

Ім'я файлу (відносний шлях).

`value`

Вміст файлу.

### Значення, що повертаються

Нічого не вертає.

### Помилки

Якщо опція [phar.readonly](phar.configuration.md#ini.phar.readonly)установлен в , то буде викинуто виняток [BadMethodCallException](class.badmethodcallexception.md), так як модифікувати Phar-архів можна тільки, якщо phar.readonly дорівнює . Якщо виникнуть якісь проблеми із записом на диск - викидається виняток [PharException](class.pharexception.md)

### Приклади

**Приклад #1 Приклад використання** Phar::offsetSet()\*\*\*\*

offsetSet не потрібно викликати безпосередньо. Використовуйте синтаксис `[]`

```php
<?php
$p = new Phar('/path/to/my.phar', 0, 'my.phar');
try {
    // вызов offsetSet
    $p['file.txt'] = 'Hi there';
} catch (Exception $e) {
    echo 'Не могу изменить file.txt:', $e;
}
?>
```

### Примітки

> **Зауваження** [Phar::addFile()](phar.addfile.md) [Phar::addFromString()](phar.addfromstring.md)и**Phar::offsetSet()** зберігає новий phar-архів щоразу під час їхнього виклику. Якщо продуктивність викликає занепокоєння, натомість слід використовувати [Phar::buildFromDirectory()](phar.buildfromdirectory.md) або [Phar::buildFromIterator()](phar.buildfromiterator.md)

### Дивіться також

-   [Phar::offsetExists()](phar.offsetexists.md) \- Визначити, чи є файл у архіві
-   [Phar::offsetGet()](phar.offsetget.md) \- Отримати PharFileInfo об'єкт для конкретного файлу
-   [Phar::offsetUnset()](phar.offsetunset.md) \- Видалити файл із phar-архіву
