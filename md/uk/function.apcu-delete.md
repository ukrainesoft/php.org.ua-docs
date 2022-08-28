Видаляє збережене значення з кешу

-   [« apcu\_dec](function.apcu-dec.html)
    
-   [apcu\_enabled »](function.apcu-enabled.html)
    
-   [PHP Manual](index.html)
    
-   [Функции APCu](ref.apcu.html)
    
-   Видаляє збережене значення з кешу
    

# apcudelete

(PECL apcu >= 4.0.0)

apcudelete — Видалення збереженого значення з кешу

### Опис

```methodsynopsis
apcu_delete(mixed $key): mixed
```

Видаляє збережене значення з кеша.

### Список параметрів

`key`

`key` можна встановити як рядок, для видалення одного значення, або як масив рядків, для видалення кількох значень, або як об'єкт [APCUIterator](class.apcuiterator.html)

### Значення, що повертаються

Якщо `key` є масивом (array), повертається індексований масив (array) ключів. В іншому випадку повертається **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **apcudelete()****

```php
<?php
$bar = 'BAR';
apcu_store('foo', $bar);

//Удаляем одну запись.
apcu_delete('foo');

// Удаляем несколько записей.
apcu_delete(['foo', 'bar', 'baz']);

// Используем итератор с регулярным выражением.
apcu_delete(new APCUIterator('#^myprefix_#'));
?>
```

### Дивіться також

-   [apcu\_store()](function.apcu-store.html) - Кешує змінну
-   [apcu\_fetch()](function.apcu-fetch.html) - Витягує з кеша збережену змінну
-   [apcu\_clear\_cache()](function.apcu-clear-cache.html) - Очистити кеш APCu
-   [APCUIterator](class.apcuiterator.html)