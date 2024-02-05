---
navigation:
  - quickhashinthash.loadfromfile.md: '« QuickHashIntHash::loadFromFile'
  - quickhashinthash.savetofile.md: 'QuickHashIntHash::saveToFile »'
  - index.md: PHP Manual
  - class.quickhashinthash.md: QuickHashIntHash
title: 'QuickHashIntHash::loadFromString'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# QuickHashIntHash::loadFromString

(PECL quickhash >= Unknown)

QuickHashIntHash::loadFromString — Фабричний метод створює хеш із рядка

### Опис

```methodsynopsis
public static QuickHashIntHash::loadFromString(string $contents, int $options = ?): QuickHashIntHash
```

Цей фабричний метод створює новий хеш із визначення у рядку. Формат файлу складається з 32-бітових цілих чисел зі знаком, запакованих разом у системний порядок байтів. Для кожного елемента зберігаються два 32-бітових цілих числа зі знаком. Перше - ключ, а друге - значення, що належить ключу.

### Список параметрів

`contents`

Рядок, що містить серіалізований формат хешу.

`options`

Ті самі параметри, які приймає конструктор класу; за винятком того, що ігнорується параметр `size`. Він автоматично обчислюється як кількість записів у хеш, округляється до найближчого ступеня числа 2 з максимальним обмеженням `4194304`

### Значення, що повертаються

Повертає новий об'єкт [QuickHashIntHash](class.quickhashinthash.md)

### Приклади

**Приклад #1 Приклад використання** QuickHashIntHash::loadFromString()\*\*\*\*

```php
<?php
$contents = file_get_contents( dirname( __FILE__ ) . "/simple.hash" );
$hash = QuickHashIntHash::loadFromString(
    $contents,
    QuickHashIntHash::DO_NOT_USE_ZEND_ALLOC
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
