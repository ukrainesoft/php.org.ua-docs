Встановити завантажувач або заглушку в Phar-архів

-   [« Phar::setSignatureAlgorithm](phar.setsignaturealgorithm.md)
    
-   [Phar::startBuffering »](phar.startbuffering.md)
    
-   [PHP Manual](index.md)
    
-   [Phar](class.phar.md)
    
-   Встановити завантажувач або заглушку в Phar-архів
    

# Phar::setStub

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

Phar::setStub — Встановити завантажувач або завантажувальну заглушку в Phar-архів

### Опис

```methodsynopsis
public Phar::setStub(string $stub, int $len = -1): bool
```

> **Зауваження**
> 
> Для коректної роботи з об'єктами [Phar](class.phar.md) цьому методу необхідне встановлення значення php.ini `phar.readonly` в `0`. В іншому випадку, буде викинуто виняток [PharException](class.pharexception.md)

Цей метод використовується для додавання початкової завантажувальної заглушки PHP (PHP bootstrap loader stub) до нового Phar-архіву або для заміни вже існуючого завантажувальної заглушки.

Завантажувач заглушки використовується при підключенні Phar-архіву за допомогою included:

```php
<?php
include 'myphar.phar';
?>
```

Завантажувач недоступний, коли архів вмикається з використанням обгортки `phar`, як у прикладі нижче:

```php
<?php
include 'phar://myphar.phar/somefile.php';
?>
```

### Список параметрів

`stub`

Рядок, або відкритий ресурс потоку.

`len`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Викидається виняток [UnexpectedValueException](class.unexpectedvalueexception.md), якщо [phar.readonly](phar.configuration.html#ini.phar.readonly) дозволено у php.ini. У разі проблем із записом на диск буде викинуто виняток [PharException](class.pharexception.md)

### Приклади

**Приклад #1 Приклад використання **Phar::setStub()****

```php
<?php
try {
    $p = new Phar(dirname(__FILE__) . '/brandnewphar.phar', 0, 'brandnewphar.phar');
    $p['a.php'] = '<?php var_dump("Hello");';
    $p->setStub('<?php var_dump("First"); Phar::mapPhar("brandnewphar.phar"); __HALT_COMPILER(); ?>');
    include 'phar://brandnewphar.phar/a.php';
    var_dump($p->getStub());
    $p['b.php'] = '<?php var_dump("World");';
    $p->setStub('<?php var_dump("Second"); Phar::mapPhar("brandnewphar.phar"); __HALT_COMPILER(); ?>');
    include 'phar://brandnewphar.phar/b.php';
    var_dump($p->getStub());
} catch (Exception $e) {
    echo 'Операции записи на brandnewphar.phar завершились неудачей: ', $e;
}
?>
```

Результат виконання цього прикладу:

```
string(5) "Hello"
string(82) "<?php var_dump("First"); Phar::mapPhar("brandnewphar.phar"); __HALT_COMPILER(); ?>"
string(5) "World"
string(83) "<?php var_dump("Second"); Phar::mapPhar("brandnewphar.phar"); __HALT_COMPILER(); ?>"
```

### Дивіться також

-   [Phar::getStub()](phar.getstub.md) - Отримати завантажувач PHP або завантажувач заглушки Phar-архіву
-   [Phar::createDefaultStub()](phar.createdefaultstub.md) - Створити заглушку у форматі phar-архіву