Перевіряє використовується стійке з'єднання з сервером memcache

-   [« Memcached::incrementByKey](memcached.incrementbykey.html)
    
-   [Memcached::isPristine »](memcached.ispristine.html)
    
-   [PHP Manual](index.html)
    
-   [Memcached](class.memcached.html)
    
-   Перевіряє використовується стійке з'єднання з сервером memcache
    

# Memcached::isPersistent

(PECL memcached >= 2.0.0)

Memcached::isPersistent — Перевіряє, чи використовується стійке з'єднання з сервером memcache

### Опис

```methodsynopsis
public Memcached::isPersistent(): bool
```

**Memcached::isPersistent()** перевіряє чи є з'єднання з серверами memcache стійким тобто. що зберігається між запитами.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає true якщо екземпляр класу Memcache використовує стійке з'єднання, і false інакше.

### Дивіться також

-   [Memcached::isPristine()](memcached.ispristine.html) - Перевіряє чи вже створено екземпляр класу Memcached