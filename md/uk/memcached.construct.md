---
navigation:
  - memcached.casbykey.md: '« Memcached::casByKey'
  - memcached.decrement.md: 'Memcached::decrement »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::\_\_construct

(PECL memcached >= 0.1.0)

Memcached::\_\_construct — Створює екземпляр класу Memcached

### Опис

public**Memcached::\_\_construct**(?string`$persistent_id` **`null`**, ?[callable](language.types.callable.md) `$callback` **`null`**, ?string`$connection_str` **`null`**) .

Створює екземпляр класу Memcached, який з'єднує з'єднання з сервером memcache.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`persistent_id`

За замовчуванням екземпляр класу Memcached знищується наприкінці запиту. Для створення екземпляра, який зберігається між запитами, необхідно використовувати `persistent_id`, щоб зазначити унікальний ідентифікатор для екземпляра. Усі екземпляри класу, створені з використанням одного і того ж ідентифікатора `persistent_id` будуть використовувати спільне з'єднання.

`callback`

`connection_str`

### Приклади

**Приклад #1 Створення екземпляра класу Memcached**

```php
<?php
/* Создаёт обычный экземпляр класса */
$m = new Memcached();
echo get_class($m);

/* Создаёт устойчивый экземпляр класса */
$m2 = new Memcached('story_pool');
$m3 = new Memcached('story_pool');

/* Теперь объекты $m2 и $m3 используют общее соединение */
?>
```
