---
navigation:
  - quickhashstringinthash.construct.md: '« QuickHashStringIntHash::\_\_construct'
  - quickhashstringinthash.exists.md: 'QuickHashStringIntHash::exists »'
  - index.md: PHP Manual
  - class.quickhashstringinthash.md: QuickHashStringIntHash
title: 'QuickHashStringIntHash::delete'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# QuickHashStringIntHash::delete

(No version information available, might only be in Git)

QuickHashStringIntHash::delete — Метод видаляє запис із хешу

### Опис

```methodsynopsis
public QuickHashStringIntHash::delete(string $key): bool
```

Метод видаляє запис з хешу і повертає, чи цей запис видалено чи ні. Відповідні структури пам'яті буде звільнено не відразу, а при звільненні самого хеша.

Елементи не можна видалити, якщо хеш використовується в ітераторі. Метод не викине виняток, а просто поверне **`false`** як це сталося б за будь-якої іншої помилки видалення.

### Список параметрів

`key`

Ключ запису, який потрібно видалити.

### Значення, що повертаються

Метод возвращает\*\*`true`\*\*, якщо запис було видалено та **`false`**, якщо запис не видалено.

### Приклади

**Приклад #1 Приклад використання** QuickHashStringIntHash::delete()\*\*\*\*

```php
<?php
$hash = new QuickHashStringIntHash( 1024 );
var_dump( $hash->exists( 'four' ) );
var_dump( $hash->add( 'four', 5 ) );
var_dump( $hash->get( 'four' ) );
var_dump( $hash->delete( 'four' ) );
var_dump( $hash->exists( 'four' ) );
var_dump( $hash->get( 'four' ) );
var_dump( $hash->delete( 'four' ) );
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(false)
bool(true)
int(5)
bool(true)
bool(false)
bool(false)
bool(false)
```
