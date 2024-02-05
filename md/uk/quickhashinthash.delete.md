---
navigation:
  - quickhashinthash.construct.md: '« QuickHashIntHash::\_\_construct'
  - quickhashinthash.exists.md: 'QuickHashIntHash::exists »'
  - index.md: PHP Manual
  - class.quickhashinthash.md: QuickHashIntHash
title: 'QuickHashIntHash::delete'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# QuickHashIntHash::delete

(PECL quickhash >= Unknown)

QuickHashIntHash::delete — Метод видаляє запис із хешу

### Опис

```methodsynopsis
public QuickHashIntHash::delete(int $key): bool
```

Метод видаляє запис з хешу і повертає, чи цей запис видалено чи ні. Відповідні структури пам'яті буде звільнено не відразу, а при звільненні самого хеша.

Елементи не можна видалити, якщо хеш використовується в ітераторі. Метод не викине виняток, а просто поверне **`false`** як це сталося б за будь-якої іншої помилки видалення.

### Список параметрів

`key`

Ключ запису, який потрібно видалити.

### Значення, що повертаються

Метод возвращает\*\*`true`\*\*, якщо запис було видалено та **`false`**, якщо запис не видалено.

### Приклади

**Пример #1 Пример использования**QuickHashIntHash::delete()\*\*\*\*

```php
<?php

$hash = new QuickHashIntHash( 1024 );
var_dump( $hash->exists( 4 ) );
var_dump( $hash->add( 4, 5 ) );
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
