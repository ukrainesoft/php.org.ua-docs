Кодує дані поточної сесії у форматі рядка сесії

-   [« session\_destroy](function.session-destroy.html)
    
-   [session\_gc »](function.session-gc.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с сессиями](ref.session.html)
    
-   Кодує дані поточної сесії у форматі рядка сесії
    

# sessionencode

(PHP 4, PHP 5, PHP 7, PHP 8)

sessionencode — Кодує дані поточної сесії у форматі рядка сесії

### Опис

```methodsynopsis
session_encode(): string|false
```

**sessionencode()** повертає серіалізований рядок, що містить дані поточної сесії, що зберігаються в суперглобальному масиві $ SESSION.

За замовчуванням використовується внутрішній метод серіалізації PHP і результат відрізнятиметься від формату, що повертається функцією [serialize()](function.serialize.html). Метод серіалізації може бути встановлений за допомогою [session.serialize\_handler](session.configuration.html#ini.session.serialize-handler)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає серіалізовані дані поточної сесії або **`false`** у разі виникнення помилки.

### Примітки

**Увага**

Необхідно викликати функцію [session\_start()](function.session-start.html) перед використанням **sessionencode()**

### Дивіться також

-   [session\_decode()](function.session-decode.html) - декодує дані сесії із закодованого рядка сесії
-   [session.serialize\_handler](session.configuration.html#ini.session.serialize-handler)