---
navigation:
  - ref.memcache.md: « Функції Memcache
  - book.memcached.md: Memcached »
  - index.md: PHP Manual
  - ref.memcache.md: Функції Memcache
title: memcache\_debug
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# memcache\_debug

(PECL memcache >= 0.2.0)

memcache\_debug — Увімкнути/вимкнути виведення налагоджувальної інформації

### Опис

```methodsynopsis
memcache_debug(bool $on_off): bool
```

**memcache\_debug()** включає висновок налагоджувальної інформації, якщо `on_off`установлен в\*\*`true`\*\* і вимикає, якщо в **`false`**

> **Зауваження** :
> 
> Функция**memcache\_debug()** доступна, тільки якщо PHP був зібраний за допомогою опції --enable-debug і в цьому випадку завжди повертає **`true`**. Інакше виклик цієї функції нічого не робить та повертає **`false`**

### Список параметрів

`on_off`

Включає виведення налагоджувальної інформації, якщо встановлено **`true`**. Вимикає висновок налагоджувальної інформації, якщо встановлено **`false`**

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо PHP був зібраний з опцією --enable-debug, інакше - **`false`**
