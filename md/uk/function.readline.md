---
navigation:
  - function.readline-write-history.html: « readlinewritehistory
  - refs.compression.md: Модулі для стиснення та архівації »
  - index.md: PHP Manual
  - ref.readline.md: Функции Readline
title: readline
---
# readline

(PHP 4, PHP 5, PHP 7, PHP 8)

readline — Читає рядок

### Опис

```methodsynopsis
readline(?string $prompt = null): string|false
```

Читає один рядок, введений користувачем. Якщо вам потрібно додати цей рядок до історії, то зробити це ви повинні самостійно, за допомогою [readlineaddhistory()](function.readline-add-history.md)

### Список параметрів

`prompt`

Підказка, яка буде виведена користувачеві.

### Значення, що повертаються

Повертає один рядок, введений користувачем. Символ кінця рядка буде видалено. Якщо більше нема даних для читання, тоді повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **readline()****

```php
<?php
//получим 3 команды от пользователя
for ($i=0; $i < 3; $i++) {
        $line = readline("Command: ");
        readline_add_history($line);
}

//распечатаем историю ввода
print_r(readline_list_history());

//распечатаем переменные
print_r(readline_info());
?>
```
