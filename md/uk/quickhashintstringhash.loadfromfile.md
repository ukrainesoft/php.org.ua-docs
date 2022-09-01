---
navigation:
  - quickhashintstringhash.getsize.md: '« QuickHashIntStringHash::getSize'
  - quickhashintstringhash.loadfromstring.md: 'QuickHashIntStringHash::loadFromString »'
  - index.md: PHP Manual
  - class.quickhashintstringhash.md: QuickHashIntStringHash
title: 'QuickHashIntStringHash::loadFromFile'
---
# QuickHashIntStringHash::loadFromFile

(PECL quickhash >= Unknown)

QuickHashIntStringHash::loadFromFile — Фабричний метод створює хеш із файлу

### Опис

```methodsynopsis
public static QuickHashIntStringHash::loadFromFile(string $filename, int $size = 0, int $options = 0): QuickHashIntStringHash
```

Цей фабричний метод створює новий хеш із файлу визначення на диску. Формат файлу складається із сигнатури `'QH\0x12\0'`Кількість елементів у вигляді 32-бітного цілого числа зі знаком у системному порядку байтів, потім 32-бітних цілих чисел зі знаком, упакованих разом у системний порядок байтів. Для кожного елемента хеша зберігаються два 32-бітових цілих числа зі знаком. Перше - ключ, а друге - значення, що належить ключу. Прикладом може бути:

**Приклад #1 Формат файлу QuickHash IntString**

```
00000000  51 48 12 00 02 00 00 00  09 00 00 00 4f 4e 45 00  |QH..........ONE.|
00000010  4e 49 4e 45 00 01 00 00  00 00 00 00 00 03 00 00  |NINE............|
00000020  00 04 00 00 00                                    |.....|
00000025
```

**Приклад #2 Формат файлу QuickHash IntString**

```
header signature ('QH'; key type: 1; value type: 2; filler: \0x00)
00000000  51 48 12 00

number of elements:
00000004  02 00 00 00

length of string values (9 characters):
00000008  09 00 00 00

string values:
0000000C  4f 4e 45 00 4e 49 4e 45  00

data string:
00000015  01 00 00 00 00 00 00 00  03 00 00 00 04 00 00 00

key/value 1 (key = 1, string index = 0 ("ONE")):
01 00 00 00  00 00 00 00

key/value 2 (key = 3, string index = 4 ("NINE")):
03 00 00 00  04 00 00 00
```

### Список параметрів

`filename`

Ім'я файлу, з якого потрібно рахувати хеш.

`size`

Кількість списків, які потрібно налаштувати. Передане число буде автоматично округлено до наступного ступеня 2. Воно також автоматично обмежується від `4` до `4194304`

`options`

Ті самі параметри, які приймає конструктор класу; за винятком того, що ігнорується параметр `size`. Він автоматично обчислюється як кількість записів у хеш, округляється до найближчого ступеня числа 2 з максимальним обмеженням `4194304`

### Значення, що повертаються

Повертає новий об'єкт [QuickHashIntStringHash](class.quickhashintstringhash.md)

### Приклади

**Приклад #3 Приклад використання **QuickHashIntStringHash::loadFromFile()****

```php
<?php
$file = dirname( __FILE__ ) . "/simple.string.hash";
$hash = QuickHashIntStringHash::loadFromFile(
    $file,
    QuickHashIntStringHash::DO_NOT_USE_ZEND_ALLOC
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
