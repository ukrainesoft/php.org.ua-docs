Створює екземпляр класу Memcached

-   [« Memcached::casByKey](memcached.casbykey.md)
    
-   [Memcached::decrement »](memcached.decrement.md)
    
-   [PHP Manual](index.md)
    
-   [Memcached](class.memcached.md)
    
-   Створює екземпляр класу Memcached
    

# Memcached::construct

(PECL memcached >= 0.1.0)

Memcached::construct — Створює екземпляр класу Memcached

### Опис

public **Memcached::construct**(string `$persistent_id`

Створює екземпляр класу Memcached, що з'єднує з сервером memcache.

### Список параметрів

`persistent_id`

За замовчуванням екземпляр класу Memcached знищується наприкінці запиту. Для створення екземпляра, який зберігається між запитами, потрібно використовувати `persistent_id`щоб вказати унікальний ідентифікатор для екземпляра. Усі екземпляри класу, створені з використанням одного і того ж ідентифікатора `persistent_id` будуть використовувати спільне з'єднання.

### Приклади

**Приклад #1 Створення екземпляра класу Memcached**

```php
<?php
/* Создаёт обычный экземпляр класса */
$m = new Memcached();
echo get_class($m);

/* Создаёт устойчивый экземпляр класса */
$m2 = new Memcached('story_pool');
$m3 = new Memcached('story_pool');

/* Теперь объекты $m2 и $m3 используют общее соединение */
?>
```