---
navigation:
  - function.setcookie.md: « setcookie
  - function.socket-get-status.md: socket\_get\_status »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: setrawcookie
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# setrawcookie

(PHP 5, PHP 7, PHP 8)

setrawcookie — Надсилає cookie без URL-кодування значення

### Опис

```methodsynopsis
setrawcookie(    string $name,    string $value = ?,    int $expires_or_options = 0,    string $path = ?,    string $domain = ?,    bool $secure = false,    bool $httponly = false): bool
```

Альтернативна сигнатура доступна з PHP 7.3.0 (іменовані параметри не підтримуються):

```methodsynopsis
setrawcookie(string $name, string $value = ?, array $options = []): bool
```

Функция**setrawcookie()** є повним аналогом функції [setcookie()](function.setcookie.md), за винятком того, що значення cookie не буде автоматично закодовано під час надсилання браузеру.

### Список параметрів

Для получения информации по параметру, смотрите документацию по функции[setcookie()](function.setcookie.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 7.3.0 | Додано альтернативний підпис, що підтримує масив опцій `options`. . Цей підпис також підтримує налаштування cookie-атрибута SameSite. |

### Дивіться також

-   [setcookie()](function.setcookie.md) \- Надсилає cookie
