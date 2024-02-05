---
navigation:
  - function.readline-callback-handler-remove.md: « readline\_callback\_handler\_remove
  - function.readline-clear-history.md: readline\_clear\_history »
  - index.md: PHP Manual
  - ref.readline.md: Опції Readline
title: readline\_callback\_read\_char
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# readline\_callback\_read\_char

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

readline\_callback\_read\_char — Читає символ та інформує callback-функцію readline, що отримано рядок

### Опис

```methodsynopsis
readline_callback_read_char(): void
```

Читає введений користувачем символ. Коли рядок отримано, ця функція інформує callback-функцію інтерфейсу readline, задану за допомогою [readline\_callback\_handler\_install()](function.readline-callback-handler-install.md), що рядок готовий до введення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

Пример использования интерфейса callback-функций readline смотрите на странице описания функции[readline\_callback\_handler\_install()](function.readline-callback-handler-install.md)

### Дивіться також

-   [readline\_callback\_handler\_install()](function.readline-callback-handler-install.md) \- Ініціалізує callback-інтерфейс readline та термінал, друкує рядок запрошення та негайно повертає управління
-   [readline\_callback\_handler\_remove()](function.readline-callback-handler-remove.md) \- Видаляє раніше зареєстровану callback-функцію та відновлює термінал
