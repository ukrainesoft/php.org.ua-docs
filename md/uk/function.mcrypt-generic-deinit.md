---
navigation:
  - function.mcrypt-encrypt.html: « mcryptencrypt
  - function.mcrypt-generic-init.html: mcryptgenericinit »
  - index.html: PHP Manual
  - ref.mcrypt.html: Mcrypt
title: mcryptgenericdeinit
---
# mcryptgenericdeinit

(PHP 4 >= 4.0.7, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcryptgenericdeinit — Ця функція деініціалізує модуль шифрування

**Увага**

Ця функція оголошена *застарілої*, починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_generic_deinit(resource $td): bool
```

Ця функція перериває шифрування, задане дескриптором шифрування (`td`). Вона очищує всі буфери, але не закриває модуль. Для закриття модуля ви повинні самостійно викликати [mcryptmoduleclose()](function.mcrypt-module-close.html), або його буде автоматично закрито після завершення роботи скрипта.

### Список параметрів

`td`

Дескриптор шифрування.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [mcryptmoduleopen()](function.mcrypt-module-open.html) - Відкриває модуль шифрування з використанням вказаних алгоритму та режиму
-   [mcryptgenericinit()](function.mcrypt-generic-init.html) - Функція ініціалізує всі буфери, необхідні для шифрування
