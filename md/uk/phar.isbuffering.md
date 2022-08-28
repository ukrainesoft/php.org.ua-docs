Перевірити, чи будуть операції з Phar-архівом буферизовані чи записані безпосередньо на диск

-   [« Phar::interceptFileFuncs](phar.interceptfilefuncs.html)
    
-   [Phar::isCompressed »](phar.iscompressed.html)
    
-   [PHP Manual](index.html)
    
-   [Phar](class.phar.html)
    
-   Перевірити, чи будуть операції з Phar-архівом буферизовані чи записані безпосередньо на диск
    

# Phar::isBuffering

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

Phar::isBuffering — Перевірити, чи будуть операції з Phar-архівом буферизовані або записані безпосередньо на диск

### Опис

```methodsynopsis
public Phar::isBuffering(): bool
```

Перевіряє, чи будуть операції з Phar-архівом одразу записані на диск чи для цього треба викликати [Phar::stopBuffering()](phar.stopbuffering.html)

Налаштування буферизації є індивідуальними для кожного архіву. Включена буферизація для `foo.phar` ніяк не впливає на режим роботи з `bar.phar`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** або **`false`**

### Приклади

**Приклад #1 Приклад використання **Phar::isBuffering()****

```php
<?php
$p = new Phar(dirname(__FILE__) . '/brandnewphar.phar', 0, 'brandnewphar.phar');
$p2 = new Phar('existingphar.phar');
$p['file1.txt'] = 'hi';
var_dump($p->isBuffering());
var_dump($p2->isBuffering());
?>
=2=
<?php
$p->startBuffering();
var_dump($p->isBuffering());
var_dump($p2->isBuffering());
$p->stopBuffering();
?>
=3=
<?php
var_dump($p->isBuffering());
var_dump($p2->isBuffering());
?>
```

Результат виконання цього прикладу:

```
bool(false)
bool(false)
=2=
bool(true)
bool(false)
=3=
bool(false)
bool(false)
```

### Дивіться також

-   [Phar::startBuffering()](phar.startbuffering.html) - Запуск буферизації операцій запису, відключаючи запис змін Phar-архіву на диск
-   [Phar::stopBuffering()](phar.stopbuffering.html) - Зупиняє буферизацію та записує всі зміни на диск