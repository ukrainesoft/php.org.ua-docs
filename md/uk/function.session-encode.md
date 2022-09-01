---
navigation:
  - function.session-destroy.html: « sessiondestroy
  - function.session-gc.html: sessiongc »
  - index.md: PHP Manual
  - ref.session.md: Функції для роботи із сесіями
title: sessionencode
---
# sessionencode

(PHP 4, PHP 5, PHP 7, PHP 8)

sessionencode — Кодує дані поточної сесії у форматі рядка сесії

### Опис

```methodsynopsis
session_encode(): string|false
```

**sessionencode()** повертає серіалізований рядок, що містить дані поточної сесії, що зберігаються в суперглобальному масиві $ SESSION.

За замовчуванням використовується внутрішній метод серіалізації PHP і результат відрізнятиметься від формату, що повертається функцією [serialize()](function.serialize.md). Метод серіалізації може бути встановлений за допомогою [session.serializehandler](session.configuration.html#ini.session.serialize-handler)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовані дані поточної сесії або **`false`** у разі виникнення помилки.

### Примітки

**Увага**

Необхідно викликати функцію [sessionstart()](function.session-start.md) перед використанням **sessionencode()**

### Дивіться також

-   [sessiondecode()](function.session-decode.md) - декодує дані сесії із закодованого рядка сесії
-   [session.serializehandler](session.configuration.html#ini.session.serialize-handler)
