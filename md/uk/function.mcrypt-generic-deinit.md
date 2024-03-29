---
navigation:
  - function.mcrypt-encrypt.md: « mcrypt\_encrypt
  - function.mcrypt-generic-init.md: mcrypt\_generic\_init »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcrypt\_generic\_deinit
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mcrypt\_generic\_deinit

(PHP 4 >= 4.0.7, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcrypt\_generic\_deinit — Ця функція деініціалізує модуль шифрування

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_generic_deinit(resource $td): bool
```

Ця функція перериває шифрування, задане дескриптором шифрування (`td`). Вона очищує всі буфери, але не закриває модуль. Для закриття модуля ви повинні самостійно викликати [mcrypt\_module\_close()](function.mcrypt-module-close.md), або його буде автоматично закрито після завершення роботи скрипта.

### Список параметрів

`td`

Дескриптор шифрування.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [mcrypt\_module\_open()](function.mcrypt-module-open.md) \- Відкриває модуль шифрування з використанням вказаних алгоритму та режиму
-   [mcrypt\_generic\_init()](function.mcrypt-generic-init.md) \- Функція ініціалізує всі буфери, необхідні для шифрування
