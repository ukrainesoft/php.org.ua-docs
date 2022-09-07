---
navigation:
  - ref.memcache.md: « Функции Memcache
  - book.memcached.md: Memcached »
  - index.md: PHP Manual
  - ref.memcache.md: Функции Memcache
title: memcachedebug
---
# memcachedebug

(PECL memcache >= 0.2.0)

memcachedebug — Увімкнути/вимкнути виведення налагоджувальної інформації

### Опис

```methodsynopsis
memcache_debug(bool $on_off): bool
```

**memcachedebug()** включає висновок налагоджувальної інформації, якщо `on_off` встановлений в **`true`** і вимикає, якщо в **`false`**

> **Зауваження**
> 
> Функція **memcachedebug()** доступна, тільки якщо PHP був зібраний за допомогою опції --enable-debug і в цьому випадку завжди повертає **`true`**. Інакше виклик цієї функції нічого не робить та повертає **`false`**

### Список параметрів

`on_off`

Включає виведення налагоджувальної інформації, якщо встановлено **`true`**. Вимикає висновок налагоджувальної інформації, якщо встановлено **`false`**

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо PHP був зібраний з опцією --enable-debug, інакше - **`false`**
