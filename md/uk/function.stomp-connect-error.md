Повертає рядок із описом останньої помилки підключення

-   [« Функции Stomp](ref.stomp.html)
    
-   [stompversion »](function.stomp-version.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Stomp](ref.stomp.html)
    
-   Повертає рядок із описом останньої помилки підключення
    

# stompconnecterror

(PECL stomp >= 0.3.0)

stompconnecterror — Повертає рядок із описом останньої помилки підключення

### Опис

```methodsynopsis
stomp_connect_error(): string
```

Повертає рядок із описом останньої помилки підключення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Рядок з описом помилки, або \*\*`null`\*\*якщо помилки не сталося.

### Приклади

**Приклад #1 Приклад використання **stompconnecterror()****

```php
<?php
$link = stomp_connect('http://localhost:61613');

if(!$link) {
    die('Ошибка соединения: ' . stomp_connect_error());
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ошибка соединения: Invalid Broker URI scheme
```