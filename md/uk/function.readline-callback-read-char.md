---
navigation:
  - function.readline-callback-handler-remove.md: « readlinecallbackhandlerremove
  - function.readline-clear-history.md: readlineclearhistory »
  - index.md: PHP Manual
  - ref.readline.md: Функции Readline
title: readlinecallbackreadchar
---
# readlinecallbackreadchar

(PHP 5> = 5.1.0, PHP 7, PHP 8)

readlinecallbackreadchar — Читає символ та інформує callback-функцію readline, що отримано рядок

### Опис

```methodsynopsis
readline_callback_read_char(): void
```

Читає введений користувачем символ. Коли рядок отримано, ця функція інформує callback-функцію інтерфейсу readline, задану за допомогою [readlinecallbackhandlerinstall()](function.readline-callback-handler-install.md), що рядок готовий до введення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

Приклад використання інтерфейсу callback-функцій readline дивіться на сторінці опису функції [readlinecallbackhandlerinstall()](function.readline-callback-handler-install.md)

### Дивіться також

-   [readlinecallbackhandlerinstall()](function.readline-callback-handler-install.md) - Ініціалізує callback-інтерфейс readline та термінал, друкує рядок запрошення та негайно повертає управління
-   [readlinecallbackhandlerremove()](function.readline-callback-handler-remove.md) - Видаляє раніше зареєстровану callback-функцію та відновлює термінал
