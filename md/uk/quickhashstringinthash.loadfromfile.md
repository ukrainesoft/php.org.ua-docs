Фабричний метод створює хеш із файлу

-   [« QuickHashStringIntHash::getSize](quickhashstringinthash.getsize.md)
    
-   [QuickHashStringIntHash::loadFromString »](quickhashstringinthash.loadfromstring.md)
    
-   [PHP Manual](index.md)
    
-   [QuickHashStringIntHash](class.quickhashstringinthash.md)
    
-   Фабричний метод створює хеш із файлу
    

# QuickHashStringIntHash::loadFromFile

(No version information available, might only be in Git)

QuickHashStringIntHash::loadFromFile — Фабричний метод створює хеш із файлу

### Опис

```methodsynopsis
public static QuickHashStringIntHash::loadFromFile(string $filename, int $size = 0, int $options = 0): QuickHashStringIntHash
```

Цей фабричний метод створює новий хеш із файлу визначення на диску. Формат файлу складається із сигнатури `'QH\0x21\0'`кількості елементів у вигляді 32-бітного цілого числа зі знаком у системному порядку байтів, 32-бітного цілого числа без знака, що містить кількість даних елемента в символах. Дані цього елемента містять усі рядки. Далі слідує інше32-бітове ціле число зі знаком, що містить кількість списків. Після заголовка та рядків слідують елементи. Вони впорядковані за списком, тому ключі не потрібно хешувати, щоб відновити хеш. Для кожного списку зберігається наступна інформація (усі як 32-бітові цілі числа): індекс списку, кількість елементів у цьому списку, а потім парами по два 32-бітові цілі числа без знака - елементи, де перший - це індекс у рядковому списку, що містить ключі, а другий – значення. Прикладом може бути:

**Приклад #1 Формат файлу QuickHash StringIntHash**

```
00000000  51 48 21 00 02 00 00 00  09 00 00 00 40 00 00 00  |QH!.........@...|
00000010  4f 4e 45 00 4e 49 4e 45  00 07 00 00 00 01 00 00  |ONE.NINE........|
00000020  00 00 00 00 00 01 00 00  00 2f 00 00 00 01 00 00  |........./......|
00000030  00 04 00 00 00 03 00 00  00                       |.........|
00000039
```

**Приклад #2 Формат файлу QuickHash IntHash**

```
header signature ('QH'; key type: 2; value type: 1; filler: \0x00)
00000000  51 48 21 00

number of elements:
00000004  02 00 00 00

length of string values (9 characters):
00000008  09 00 00 00

number of hash bucket lists (this is configured for hashes as argument to the
constructor normally, 64 in this case):
0000000C  40 00 00 00

string values:
00000010  4f 4e 45 00 4e 49 4e 45  00

bucket lists:
  bucket list 1 (with key 7, and 1 element):
    header:
    07 00 00 00 01 00 00 00
    elements (key index: 0 ('ONE'), value = 0):
    00 00 00 00 01 00 00 00
  bucket list 2 (with key 0x2f, and 1 element):
    header:
    2f 00 00 00 01 00 00 00
    elements (key index: 4 ('NINE'), value = 3):
    04 00 00 00 03 00 00 00
```

### Список параметрів

`filename`

Ім'я файлу, з якого потрібно рахувати хеш.

`size`

Кількість списків, які потрібно налаштувати. Передане число буде автоматично округлено до наступного ступеня 2. Воно також автоматично обмежується від `4` до `4194304`

`options`

Ті самі параметри, які приймає конструктор класу; за винятком того, що ігнорується параметр `size`. Розмір зчитується з формату файлу (на відміну класів [QuickHashIntHash](class.quickhashinthash.md) і [QuickHashIntStringHash](class.quickhashintstringhash.md)де він автоматично обчислюється з кількості записів у хеші).

### Значення, що повертаються

Повертає новий об'єкт [QuickHashStringIntHash](class.quickhashstringinthash.md)

### Приклади

**Приклад #3 Приклад використання **QuickHashStringIntHash::loadFromFile()****

```php
<?php
$file = dirname( __FILE__ ) . "/simple.hash.string";
$hash = QuickHashStringIntHash::loadFromFile(
    $file,
    QuickHashStringIntHash::DO_NOT_USE_ZEND_ALLOC
);
foreach( range( 0, 0x0f ) as $key )
{
    $i = 48712 + $key * 1631;
    $k = base_convert( $i, 10, 36 );
    echo $k, ' => ', $hash->get( $k ), "\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
11l4 => 48712
12uf => 50343
143q => 51974
15d1 => 53605
16mc => 55236
17vn => 56867
194y => 58498
1ae9 => 60129
1bnk => 61760
1cwv => 63391
1e66 => 65022
1ffh => 66653
1gos => 68284
1hy3 => 69915
1j7e => 71546
1kgp => 73177
```