---
navigation:
  - function.stream-bucket-new.md: « stream\_bucket\_new
  - function.stream-context-create.md: stream\_context\_create »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_bucket\_prepend
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_bucket\_prepend

(PHP 5, PHP 7, PHP 8)

stream\_bucket\_prepend — Додає бакет на початок бригади.

### Опис

```methodsynopsis
stream_bucket_prepend(resource $brigade, object $bucket): void
```

Функція може бути використана для додавання бакета на початок бригади бакетів. Зазвичай вона викликається з методу [php\_user\_filter::filter()](php-user-filter.filter.md)

### Список параметрів

`brigade`

`brigade` - Ресурс, що вказує на `бригаду бакетів`яка містить один або кілька об'єктів `bucket`

`bucket`

Бакет.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклади використання **stream\_bucket\_prepend()****

```php
<?php

class foo extends php_user_filter {
  protected $calls = 0;
  public function filter($in, $out, &$consumed, $closing) {
    while ($bucket = stream_bucket_make_writeable($in)) {
      $consumed += $bucket->datalen;
      if ($this->calls++ == 2) {
        // Бакет снова появится перед любым другим бакетом.
        stream_bucket_prepend($in, $bucket);
      }
    }
    return PSFS_FEED_ME;
  }
}
stream_filter_register('test', 'foo');
print  file_get_contents('php://filter/read=test/resource=foo');
?>
```
