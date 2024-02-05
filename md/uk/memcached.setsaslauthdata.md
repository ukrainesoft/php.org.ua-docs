---
navigation:
  - memcached.setoptions.md: '« Memcached::setOptions'
  - memcached.touch.md: 'Memcached::touch »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::setSaslAuthData'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::setSaslAuthData

(PECL memcached >= 2.0.0)

Memcached::setSaslAuthData — Встановлює облікові дані для автентифікації

### Опис

```methodsynopsis
public Memcached::setSaslAuthData(string $username, string $password): bool
```

**Memcached::setSaslAuthData()** встановлює ім'я користувача та пароль, які мають бути використані для SASL аутентифікації із серверами memcache.

*Цей метод доступний лише у випадку, якщо модуль memcached зібраний за допомогою SASL.* Зверніться до розділу [установка Memcached](memcached.setup.md), щоб дізнатися, як це зробити.

### Список параметрів

`username`

Ім'я користувача для автентифікації.

`password`

Пароль для автентифікації.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
