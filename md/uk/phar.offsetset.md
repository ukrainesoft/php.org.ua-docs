Зміна вмісту файлу

-   [« Phar::offsetGet](phar.offsetget.html)
    
-   [Phar::offsetUnset »](phar.offsetunset.html)
    
-   [PHP Manual](index.html)
    
-   [Phar](class.phar.html)
    
-   Зміна вмісту файлу
    

# Phar::offsetSet

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

Phar::offsetSet — Зміна вмісту файлу

### Опис

```methodsynopsis
public Phar::offsetSet(string $localName, resource|string $value): void
```

> **Зауваження**
> 
> Для коректної роботи з об'єктами [Phar](class.phar.html) цьому методу необхідне встановлення значення php.ini `phar.readonly` в `0`. В іншому випадку, буде викинуто виняток [PharException](class.pharexception.html)

Це реалізація інтерфейсу [ArrayAccess](class.arrayaccess.html)дозволяє маніпулювати вмістом Phar-архіву в стилі доступу до елементів масиву. offsetSet використовується для зміни контенту існуючого файлу або для створення нового.

### Список параметрів

`localName`

Назва файлу (відносний шлях).

`value`

Вміст файлу.

### Значення, що повертаються

Нічого не вертає.

### Помилки

Якщо опція [phar.readonly](phar.configuration.html#ini.phar.readonly) встановлений в `1`, то буде викинуто виняток [BadMethodCallException](class.badmethodcallexception.html)Так як модифікувати Phar-архів можна тільки, якщо phar.readonly дорівнює `0`. Якщо виникнуть якісь проблеми із записом на диск - викидається виняток [PharException](class.pharexception.html)

### Приклади

**Приклад #1 Приклад використання **Phar::offsetSet()****

offsetSet не потрібно викликати безпосередньо. Використовуйте синтаксис `[]`

```php
<?php
$p = new Phar('/path/to/my.phar', 0, 'my.phar');
try {
    // вызов offsetSet
    $p['file.txt'] = 'Hi there';
} catch (Exception $e) {
    echo 'Не могу изменить file.txt:', $e;
}
?>
```

### Примітки

> **Зауваження** [Phar::addFile()](phar.addfile.html) [Phar::addFromString()](phar.addfromstring.html) і **Phar::offsetSet()** зберігає новий phar-архів щоразу при їхньому викликі. Якщо продуктивність викликає занепокоєння, натомість слід використовувати [Phar::buildFromDirectory()](phar.buildfromdirectory.html) або [Phar::buildFromIterator()](phar.buildfromiterator.html)

### Дивіться також

-   [Phar::offsetExists()](phar.offsetexists.html) - Визначити, чи є файл у архіві
-   [Phar::offsetGet()](phar.offsetget.html) - Отримати PharFileInfo об'єкт для конкретного файлу
-   [Phar::offsetUnset()](phar.offsetunset.html) - Видалити файл із phar-архіву