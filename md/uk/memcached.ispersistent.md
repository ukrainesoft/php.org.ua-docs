---
navigation:
  - memcached.incrementbykey.md: '« Memcached::incrementByKey'
  - memcached.ispristine.md: 'Memcached::isPristine »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::isPersistent'
---
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

-   [Memcached::isPristine()](memcached.ispristine.md) - Перевіряє чи вже створено екземпляр класу Memcached
