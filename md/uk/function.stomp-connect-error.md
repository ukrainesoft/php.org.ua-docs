---
navigation:
  - ref.stomp.md: « Функції Stomp
  - function.stomp-version.md: stomp\_version »
  - index.md: PHP Manual
  - ref.stomp.md: Опції Stomp
title: stomp\_connect\_error
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stomp\_connect\_error

(PECL stomp >= 0.3.0)

stomp\_connect\_error — Повертає рядок із описом останньої помилки підключення

### Опис

```methodsynopsis
stomp_connect_error(): string
```

Повертає рядок із описом останньої помилки підключення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Строка с описанием ошибки, или\*\*`null`\*\*якщо помилки не сталося.

### Приклади

**Пример #1 Пример использования**stomp\_connect\_error()\*\*\*\*

```php
<?php
$link = stomp_connect('http://localhost:61613');

if(!$link) {
    die('Ошибка соединения: ' . stomp_connect_error());
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ошибка соединения: Invalid Broker URI scheme
```
