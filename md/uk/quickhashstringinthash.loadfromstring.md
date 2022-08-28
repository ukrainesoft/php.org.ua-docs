Фабричний метод створює хеш із рядка

-   [« QuickHashStringIntHash::loadFromFile](quickhashstringinthash.loadfromfile.html)
    
-   [QuickHashStringIntHash::saveToFile »](quickhashstringinthash.savetofile.html)
    
-   [PHP Manual](index.html)
    
-   [QuickHashStringIntHash](class.quickhashstringinthash.html)
    
-   Фабричний метод створює хеш із рядка
    

# QuickHashStringIntHash::loadFromString

(No version information available, might only be in Git)

QuickHashStringIntHash::loadFromString — Фабричний метод створює хеш із рядка

### Опис

```methodsynopsis
public static QuickHashStringIntHash::loadFromString(string $contents, int $size = 0, int $options = 0): QuickHashStringIntHash
```

Цей фабричний метод створює новий хеш із визначення у рядку. Формат такий самий, як і в [QuickHashStringIntHash::loadFromFile()](quickhashstringinthash.loadfromfile.html)

### Список параметрів

`contents`

Рядок, що містить серіалізований формат хешу.

`size`

Кількість списків, які потрібно налаштувати. Число, що передається, буде автоматично округлено до наступного ступеня числа два. Воно також автоматично обмежується від `4` до `4194304`

`options`

Ті самі параметри, які приймає конструктор класу; за винятком того, що ігнорується параметр `size`. Він автоматично обчислюється як кількість записів у хеш, округляється до найближчого ступеня числа 2 з максимальним обмеженням `4194304`

### Значення, що повертаються

Повертає новий об'єкт [QuickHashStringIntHash](class.quickhashstringinthash.html)

### Приклади

**Приклад #1 Приклад використання **QuickHashStringIntHash::loadFromString()****

```php
<?php
$contents = file_get_contents( dirname( __FILE__ ) . "/simple.hash.string" );
$hash = QuickHashStringIntHash::loadFromString(
    $contents,
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