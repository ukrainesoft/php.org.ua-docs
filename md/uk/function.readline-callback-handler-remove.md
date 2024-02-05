---
navigation:
  - function.readline-callback-handler-install.md: « readline\_callback\_handler\_install
  - function.readline-callback-read-char.md: readline\_callback\_read\_char »
  - index.md: PHP Manual
  - ref.readline.md: Опції Readline
title: readline\_callback\_handler\_remove
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# readline\_callback\_handler\_remove

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

readline\_callback\_handler\_remove — Видаляє раніше зареєстровану callback-функцію та відновлює термінал

### Опис

```methodsynopsis
readline_callback_handler_remove(): bool
```

Видаляє раніше зареєстровану callback-функцію та відновлює налаштування терміналу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, если удаление прошло успешно или\*\*`false`\*\*, якщо видаляти нічого.

### Приклади

Приклад использования интерфейса callback-функций readline смотрите на странице описания функции[readline\_callback\_handler\_install()](function.readline-callback-handler-install.md)

### Дивіться також

-   [readline\_callback\_handler\_install()](function.readline-callback-handler-install.md) \- Ініціалізує callback-інтерфейс readline та термінал, друкує рядок запрошення та негайно повертає управління
-   [readline\_callback\_read\_char()](function.readline-callback-read-char.md) \- Читає символ та інформує callback-функцію readline, що отримано рядок
