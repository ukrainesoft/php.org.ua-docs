---
navigation:
  - phar.startbuffering.md: '« Phar::startBuffering'
  - phar.unlinkarchive.md: 'Phar::unlinkArchive »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::stopBuffering'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Phar::stopBuffering

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

Phar::stopBuffering — Зупиняє буферизацію та записує всі зміни на диск

### Опис

```methodsynopsis
public Phar::stopBuffering(): void
```

Метод**Phar::stopBuffering()** використовується спільно з методом [Phar::startBuffering()](phar.startbuffering.md). . [Phar::startBuffering()](phar.startbuffering.md) може дати значний приріст продуктивності під час створення, чи модифікації phar-архіва з великою кількістю файлів. Зазвичай, коли додається новий файл або змінюється існуючий, запускається операція перестворення phar-архіву. З увімкненою буферизацією архів буде перетворено один раз наприкінці внесення змін.

Ця концепція працює аналогічно транзакції в базі даних, що дозволяє зробити поза необхідні зміни та застосувати їх одночасно, в рамках однієї операції. Така поведінка забезпечує пару методів [Phar::startBuffering()](phar.startbuffering.md) **Phar::stopBuffering()**

Налаштування буферизації є індивідуальними для кожного архіву. Включена буферизація для `foo.phar` ніяк не впливає на режим роботи з `bar.phar`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

У разі проблем із записом на диск буде викинуто виняток [PharException](class.pharexception.md)

### Приклади

**Пример #1 Пример использования**Phar::stopBuffering()\*\*\*\*

```php
<?php
$p = new Phar(dirname(__FILE__) . '/brandnewphar.phar', 0, 'brandnewphar.phar');
$p['file1.txt'] = 'hi';
$p->startBuffering();
var_dump($p->getStub());
$p->setStub("<?php
function __autoload(\$class)
{
    include 'phar://brandnewphar.phar/' . str_replace('_', '/', \$class) . '.php';
}
Phar::mapPhar('brandnewphar.phar');
include 'phar://brandnewphar.phar/startup.php';
__HALT_COMPILER();");
$p->stopBuffering();
var_dump($p->getStub());
?>
```

Результат виконання наведеного прикладу:

```
string(24) "<?php __HALT_COMPILER();"
string(195) "<?php
function __autoload($class)
{
    include 'phar://' . str_replace('_', '/', $class);
}
Phar::mapPhar('brandnewphar.phar');
include 'phar://brandnewphar.phar/startup.php';
__HALT_COMPILER();"
```

### Дивіться також

-   [Phar::startBuffering()](phar.startbuffering.md) \- Запускає буферизацію операцій запису, відключаючи запис змін Phar-архіву на диск
-   [Phar::isBuffering()](phar.isbuffering.md) \- Перевірити, чи будуть операції з Phar-архівом буферизовані чи записані безпосередньо на диск
