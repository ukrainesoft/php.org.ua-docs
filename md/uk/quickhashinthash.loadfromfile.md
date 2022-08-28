Фабричний метод створює хеш із файлу

-   [« QuickHashIntHash::getSize](quickhashinthash.getsize.html)
    
-   [QuickHashIntHash::loadFromString »](quickhashinthash.loadfromstring.html)
    
-   [PHP Manual](index.html)
    
-   [QuickHashIntHash](class.quickhashinthash.html)
    
-   Фабричний метод створює хеш із файлу
    

# QuickHashIntHash::loadFromFile

(PECL quickhash >= Unknown)

QuickHashIntHash::loadFromFile — Фабричний метод створює хеш із файлу

### Опис

```methodsynopsis
public static QuickHashIntHash::loadFromFile(string $filename, int $options = ?): QuickHashIntHash
```

Цей фабричний метод створює новий хеш із файлу визначення на диску. Формат файлу складається із сигнатури `'QH\0x11\0'`Кількість елементів у вигляді 32-бітного цілого числа зі знаком у системному порядку байтів, потім 32-бітних цілих чисел зі знаком, упакованих разом у системний порядок байтів. Для кожного елемента хеша зберігаються два 32-бітових цілих числа зі знаком. Перше - ключ, а друге - значення, що належить ключу. Прикладом може бути:

**Приклад #1 Формат файлу QuickHash IntHash**

```
00000000  51 48 11 00 02 00 00 00  01 00 00 00 01 00 00 00  |QH..............|
00000010  03 00 00 00 09 00 00 00                           |........|
00000018
```

**Приклад #2 Формат файлу QuickHash IntHash**

```
header signature ('QH'; key type: 1; value type: 1; filler: \0x00)
00000000  51 48 11 00

number of elements:
00000004  02 00 00 00

data string:
00000000  01 00 00 00 01 00 00 00  03 00 00 00 09 00 00 00

key/value 1 (key = 1, value = 1)
01 00 00 00  01 00 00 00

key/value 2 (key = 3, value = 9)
03 00 00 00  09 00 00 00
```

### Список параметрів

`filename`

Ім'я файлу, з якого потрібно рахувати хеш.

`options`

Ті самі параметри, які приймає конструктор класу; за винятком того, що ігнорується параметр `size`. Він автоматично обчислюється як кількість записів у хеш, округляється до найближчого ступеня числа 2 з максимальним обмеженням `4194304`

### Значення, що повертаються

Повертає новий об'єкт [QuickHashIntHash](class.quickhashinthash.html)

### Приклади

**Приклад #3 Приклад використання **QuickHashIntHash::loadFromFile()****

```php
<?php
$file = dirname( __FILE__ ) . "/simple.hash";
$hash = QuickHashIntHash::loadFromFile(
    $file,
    QuickHashIntHash::DO_NOT_USE_ZEND_ALLOC
);
foreach( range( 0, 0x0f ) as $key )
{
    printf( "Ключ %3d (%2x) %s\n",
        $key, $key,
        $hash->exists( $key ) ? 'установлен' : 'не установлен'
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