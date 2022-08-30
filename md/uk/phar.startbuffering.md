Запуск буферизації операцій запису, відключаючи запис змін Phar-архіву на диск

-   [« Phar::setStub](phar.setstub.md)
    
-   [Phar::stopBuffering »](phar.stopbuffering.md)
    
-   [PHP Manual](index.md)
    
-   [Phar](class.phar.md)
    
-   Запуск буферизації операцій запису, відключаючи запис змін Phar-архіву на диск
    

# Phar::startBuffering

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

Phar::startBuffering — Запускає буферизацію операцій запису, відключаючи запис змін Phar-архіву на диск

### Опис

```methodsynopsis
public Phar::startBuffering(): void
```

Метод **Phar::startBuffering()** може дати значний приріст продуктивності під час створення, чи модифікації phar-архіва з великою кількістю файлів. Зазвичай, коли додається новий файл або змінюється існуючий, запускається операція перестворення phar-архіву. З увімкненою буферизацією архів буде перетворено один раз наприкінці внесення змін.

Ця концепція працює аналогічно транзакції в базі даних, що дозволяє зробити поза необхідні зміни та застосувати їх одночасно, в рамках однієї операції. Така поведінка забезпечує пару методів **Phar::startBuffering()**[Phar::stopBuffering()](phar.stopbuffering.md)

Налаштування буферизації є індивідуальними для кожного архіву. Включена буферизація для `foo.phar` ніяк не впливає на режим роботи з `bar.phar`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **Phar::startBuffering()****

```php
<?php
// удалим на всякий случай
@unlink('brandnewphar.phar');
try {
    $p = new Phar(dirname(__FILE__) . '/brandnewphar.phar', 0, 'brandnewphar.phar');
} catch (Exception $e) {
    echo 'не могу создать phar:', $e;
}
echo 'В новом phar содержится ' . $p->count() . " записей\n";
$p->startBuffering();
$p['file.txt'] = 'hi';
$p['file2.txt'] = 'there';
$p['file2.txt']->setCompressedGZ();
$p['file3.txt'] = 'babyface';
$p['file3.txt']->setMetadata(42);
$p->setStub("<?php
function __autoload($class)
{
    include 'phar://myphar.phar/' . str_replace('_', '/', $class) . '.php';
}
Phar::mapPhar('myphar.phar');
include 'phar://myphar.phar/startup.php';
__HALT_COMPILER();");
$p->stopBuffering();
?>
```

### Дивіться також

-   [Phar::stopBuffering()](phar.stopbuffering.md) - Зупиняє буферизацію та записує всі зміни на диск
-   [Phar::isBuffering()](phar.isbuffering.md) - Перевірити, чи будуть операції з Phar-архівом буферизовані чи записані безпосередньо на диск