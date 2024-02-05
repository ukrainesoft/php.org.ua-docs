---
navigation:
  - function.session-destroy.md: « session\_destroy
  - function.session-gc.md: session\_gc »
  - index.md: PHP Manual
  - ref.session.md: Функції для роботи із сесіями
title: session\_encode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# session\_encode

(PHP 4, PHP 5, PHP 7, PHP 8)

session\_encode — Кодує дані поточної сесії у форматі рядка сесії

### Опис

```methodsynopsis
session_encode(): string|false
```

**session\_encode()** повертає серіалізований рядок, що містить дані поточної сесії, що зберігаються в суперглобальному масиві $ \_SESSION.

За замовчуванням використовується внутрішній метод серіалізації PHP і результат відрізнятиметься від формату, що повертається функцією [serialize()](function.serialize.md). Метод серіалізації може бути встановлений за допомогою [session.serialize\_handler](session.configuration.md#ini.session.serialize-handler)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовані дані поточної сесії або \*\*`false`\*\*в случае возникновения ошибки.

### Примітки

**Увага**

Необхідно викликати функцію [session\_start()](function.session-start.md)перед использованием**session\_encode()**

### Дивіться також

-   [session\_decode()](function.session-decode.md) \- декодує дані сесії із закодованого рядка сесії
-   [session.serialize\_handler](session.configuration.md#ini.session.serialize-handler)
