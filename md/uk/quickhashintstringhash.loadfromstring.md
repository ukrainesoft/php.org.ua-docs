---
navigation:
  - quickhashintstringhash.loadfromfile.md: '« QuickHashIntStringHash::loadFromFile'
  - quickhashintstringhash.savetofile.md: 'QuickHashIntStringHash::saveToFile »'
  - index.md: PHP Manual
  - class.quickhashintstringhash.md: QuickHashIntStringHash
title: 'QuickHashIntStringHash::loadFromString'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# QuickHashIntStringHash::loadFromString

(PECL quickhash >= Unknown)

QuickHashIntStringHash::loadFromString — Фабричний метод створює хеш із рядка

### Опис

```methodsynopsis
public static QuickHashIntStringHash::loadFromString(string $contents, int $size = 0, int $options = 0): QuickHashIntStringHash
```

Цей фабричний метод створює новий хеш із визначення у рядку. Формат такий самий, як і в [QuickHashIntStringHash::loadFromFile()](quickhashintstringhash.loadfromfile.md)

### Список параметрів

`contents`

Рядок, що містить серіалізований формат хешу.

`size`

Кількість списків, які потрібно налаштувати. Число, що передається, буде автоматично округлено до наступного ступеня числа два. Воно також автоматично обмежується від `4`до`4194304`

`options`

Ті самі параметри, які приймає конструктор класу; за винятком того, що ігнорується параметр `size`. Він автоматично обчислюється як кількість записів у хеш, округляється до найближчого ступеня числа 2 з максимальним обмеженням `4194304`

### Значення, що повертаються

Повертає новий об'єкт [QuickHashIntStringHash](class.quickhashintstringhash.md)

### Приклади

**Приклад #1 Приклад використання** QuickHashIntStringHash::loadFromString()\*\*\*\*

```php
<?php
$contents = file_get_contents( dirname( __FILE__ ) . "/simple.hash" );
$hash = QuickHashIntStringHash::loadFromString(
    $contents,
    QuickHashIntStringHash::DO_NOT_USE_ZEND_ALLOC
);
foreach( range( 0, 0x0f ) as $key )
{
    printf( "Ключ %3d (%2x) %s\n",
        $key, $key,
        $hash->exists( $key ) ? 'установлен' : 'не установлен'
    );
}
?>
```

Висновок наведеного прикладу буде схожим на:

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
