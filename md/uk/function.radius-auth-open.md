Створює дескриптор Radius для автентифікації

-   [« radius\_add\_server](function.radius-add-server.html)
    
-   [radius\_close »](function.radius-close.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Radius](ref.radius.html)
    
-   Створює дескриптор Radius для автентифікації
    

# radiusauthopen

(PECL radius >= 1.1.0)

radiusauthopen — Створює дескриптор Radius для автентифікації

### Опис

```methodsynopsis
radius_auth_open(): resource
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає дескриптор у разі успішного виконання або **`false`** у разі виникнення помилки. Функція завершиться з помилкою, лише якщо недостатньо пам'яті.

### Приклади

**Приклад #1 Приклад використання **radiusauthopen()****

```php
<?php
$radh = radius_auth_open()
    or die ("Не удалось создать дескриптор");
echo "Дескриптор успешно создан";
?>
```