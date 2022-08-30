Фабричний метод створює набір із файлу

-   [« QuickHashIntSet::getSize](quickhashintset.getsize.md)
    
-   [QuickHashIntSet::loadFromString »](quickhashintset.loadfromstring.md)
    
-   [PHP Manual](index.md)
    
-   [QuickHashIntSet](class.quickhashintset.md)
    
-   Фабричний метод створює набір із файлу
    

# QuickHashIntSet::loadFromFile

(PECL quickhash >= Unknown)

QuickHashIntSet::loadFromFile — Фабричний метод створює набір із файлу

### Опис

```methodsynopsis
public static QuickHashIntSet::loadFromFile(string $filename, int $size = ?, int $options = ?): QuickHashIntSet
```

Цей фабричний метод створює новий набір файлу визначення на диску. Формат файлу складається з 32-бітових цілих чисел зі знаком, запакованих разом у системний порядок байтів.

### Список параметрів

`filename`

Ім'я файлу, з якого зчитуватиметься набір.

`size`

Кількість списків, які потрібно налаштувати. Вказане число буде автоматично округлено до наступного ступеня 2. Воно також автоматично обмежується від `4` до `4194304`

`options`

Ті самі параметри, які приймає конструктор класу; за винятком того, що ігнорується параметр `size`. Він автоматично обчислюється як кількість записів у хеш, округляється до найближчого ступеня числа 2 з максимальним обмеженням `4194304`

### Значення, що повертаються

Повертає новий об'єкт [QuickHashIntSet](class.quickhashintset.md)

### Приклади

**Приклад #1 Приклад використання **QuickHashIntSet::loadFromFile()****

```php
<?php
$file = dirname( __FILE__ ) . "/simple.set";
$set = QuickHashIntSet::loadFromFile(
    $file,
    QuickHashIntSet::DO_NOT_USE_ZEND_ALLOC
);
foreach( range( 0, 0x0f ) as $key )
{
    printf( "Ключ %3d (%2x) %s\n",
        $key, $key,
        $set->exists( $key ) ? 'установлен' : 'не установлен'
    );
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ключ   0 ( 0) не установлен
Ключ   1 ( 1) установлен
Ключ   2 ( 2) установлен
Ключ   3 ( 3) установлен
Ключ   4 ( 4) не установлен
Ключ   5 ( 5) установлен
Ключ   6 ( 6) не установлен
Ключ   7 ( 7) установлен
Ключ   8 ( 8) не установлен
Ключ   9 ( 9) не установлен
Ключ  10 ( a) не установлен
Ключ  11 ( b) установлен
Ключ  12 ( c) не установлен
Ключ  13 ( d) установлен
Ключ  14 ( e) не установлен
Ключ  15 ( f) не установлен
```