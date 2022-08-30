Прочитати поточний запущений phar-архів та зареєструвати його маніфест

-   [« Phar::loadPhar](phar.loadphar.md)
    
-   [Phar::mount »](phar.mount.md)
    
-   [PHP Manual](index.md)
    
-   [Phar](class.phar.md)
    
-   Прочитати поточний запущений phar-архів та зареєструвати його маніфест
    

# Phar::mapPhar

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

Phar::mapPhar — Прочитати поточний запущений phar-архів та зареєструвати його маніфест

### Опис

```methodsynopsis
final public static Phar::mapPhar(?string $alias = null, int $offset = 0): bool
```

Цей статичний метод можна використовувати тільки в заглушці завантажувача Phar-архіву з метою ініціалізації, коли він запущений безпосередньо, або включений в інший скрипт.

### Список параметрів

`alias`

Псевдонім можна використовувати в обгортках `phar://`, посилаючись на цей архів замість використання повного шляху.

`offset`

Змінна, що не використовується. Існує лише для сумісності з PEAR-пакетом PHPArchive.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Викидається виняток [PharException](class.pharexception.md), якщо викликається зі скрипту, в якому не виявлено токена HALTCOMPILER(); або якщо файл недоступний для читання.

### Приклади

**Приклад #1 Приклад використання **Phar::mapPhar()****

Phar::mapPhar слід використовувати лише всередині завантажувача заглушки Phar-архіву. Використовуйте loadPhar для завантаження зовнішнього phar у пам'ять.

Простий завантажувач Phar, який використовує mapPhar.

```php
<?php
function __autoload($class)
{
    include 'phar://me.phar/' . str_replace('_', '/', $class) . '.php';
}
try {
    Phar::mapPhar('me.phar');
    include 'phar://me.phar/startup.php';
} catch (PharException $e) {
    echo $e->getMessage();
    die('Cannot initialize Phar');
}
__HALT_COMPILER();
```

### Дивіться також

-   [Phar::loadPhar()](phar.loadphar.md) - Завантажити phar-архів із псевдонімом