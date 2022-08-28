Портоване блокування файлу

-   [« SplFileObject::fgetss](splfileobject.fgetss.html)
    
-   [SplFileObject::fpassthru »](splfileobject.fpassthru.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileObject](class.splfileobject.html)
    
-   Портоване блокування файлу
    

# SplFileObject::flock

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplFileObject::flock — Портоване блокування файлу

### Опис

```methodsynopsis
public SplFileObject::flock(int $operation, int &$wouldBlock = null): bool
```

Блокує або розблокує файл тим же портованим способом, що і [flock()](function.flock.html)

### Список параметрів

`operation`

`operation` може приймати такі значення:

-   **`LOCK_SH`** для отримання блокування, що розділяється (читання).
-   **`LOCK_EX`** для отримання ексклюзивного блокування (запис).
-   **`LOCK_UN`** для зняття блокування (розділюваного або ексклюзивного).

Також можна додати **`LOCK_NB`** як бітова маска до однієї з вищевказаних операцій, якщо [flock()](function.flock.html) під час спроби блокування не повинен блокуватися.

`wouldBlock`

Буде встановлений **`true`**, якщо блокування буде блокуючим (код помилки EWOULDBLOCK).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SplFileObject::flock()****

```php
<?php
$file = new SplFileObject("/tmp/lock.txt", "w");
if ($file->flock(LOCK_EX)) { // выполняем эксклюзивную блокировку
    $file->ftruncate(0);     // очищаем файл
    $file->fwrite("Что-нибудь пишем сюда\n");
    $file->flock(LOCK_UN);   // снимаем блокировку
} else {
    echo "Не удалось получить блокировку!";
}
?>
```

### Дивіться також

-   [flock()](function.flock.html) - Портоване консультативне блокування файлів