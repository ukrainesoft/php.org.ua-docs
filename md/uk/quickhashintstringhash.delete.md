---
navigation:
  - quickhashintstringhash.construct.md: '« QuickHashIntStringHash::\_\_construct'
  - quickhashintstringhash.exists.md: 'QuickHashIntStringHash::exists »'
  - index.md: PHP Manual
  - class.quickhashintstringhash.md: QuickHashIntStringHash
title: 'QuickHashIntStringHash::delete'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# QuickHashIntStringHash::delete

(PECL quickhash >= Unknown)

QuickHashIntStringHash::delete — Метод видаляє запис із хешу

### Опис

```methodsynopsis
public QuickHashIntStringHash::delete(int $key): bool
```

Метод видаляє запис з хешу і повертає, чи цей запис видалено чи ні. Відповідні структури пам'яті буде звільнено не відразу, а при звільненні самого хеша.

Елементи не можна видалити, якщо хеш використовується в ітераторі. Метод не викине виняток, а просто поверне **`false`**, як це сталося б за будь-якої іншої помилки видалення.

### Список параметрів

`key`

Ключ запису, що видаляється.

### Значення, що повертаються

Метод возвращает\*\*`true`\*\*, якщо запис було видалено та **`false`**, якщо запис не видалено.

### Приклади

**Приклад #1 Приклад використання** QuickHashIntStringHash::delete()\*\*\*\*

```php
<?php
$hash = new QuickHashIntStringHash( 1024 );
var_dump( $hash->exists( 4 ) );
var_dump( $hash->add( 4, "five" ) );
var_dump( $hash->delete( 4 ) );
var_dump( $hash->exists( 4 ) );
var_dump( $hash->delete( 4 ) );
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(false)
bool(true)
bool(true)
bool(false)
bool(false)
```
