---
navigation:
  - function.stream-bucket-new.html: « streambucketnew
  - function.stream-context-create.html: streamcontextcreate »
  - index.html: PHP Manual
  - ref.stream.html: Функції для роботи з потоками
title: streambucketprepend
---
# streambucketprepend

(PHP 5, PHP 7, PHP 8)

streambucketprepend — Додати відро на початок бригади

### Опис

```methodsynopsis
stream_bucket_prepend(resource $brigade, object $bucket): void
```

Ця функція може використовуватися для додавання відра на початок бригади відер. Зазвичай вона викликається з [phpuserfilter::filter()](php-user-filter.filter.html)

### Список параметрів

`brigade`

`brigade` - Ресурс, що вказує на `бригаду вёдер`яка містить один або кілька об'єктів `bucket`

`bucket`

Відро.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклади використання **streambucketprepend()****

```php
<?php

class foo extends php_user_filter {
  protected $calls = 0;
  public function filter($in, $out, &$consumed, $closing) {
    while ($bucket = stream_bucket_make_writeable($in)) {
      $consumed += $bucket->datalen;
      if ($this->calls++ == 2) {
        // Это ведро снова появится перед любым другим ведром.
        stream_bucket_prepend($in, $bucket);
      }
    }
    return PSFS_FEED_ME;
  }
}
stream_filter_register('test', 'foo');
print  file_get_contents('php://filter/read=test/resource=foo');
?>
```
