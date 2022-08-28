Визначає, чи позначений об'єкт як сміття

-   [« Collectable](class.collectable.html)
    
-   [Pool »](class.pool.html)
    
-   [PHP Manual](index.html)
    
-   [Collectable](class.collectable.html)
    
-   Визначає, чи позначений об'єкт як сміття
    

# Collectable::isGarbage

(PECL pthreads >= 2.0.8)

Collectable::isGarbage — Визначає, чи позначений об'єкт як сміття

### Опис

```methodsynopsis
public Collectable::isGarbage(): bool
```

Можна викликати в [Pool::collect()](pool.collect.html) визначення, чи є об'єкт сміттям.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція завжди повертає **`true`**

### Дивіться також

-   [Pool::collect()](pool.collect.html) - Збирає посилання на виконані завдання