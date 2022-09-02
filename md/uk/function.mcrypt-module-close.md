---
navigation:
  - function.mcrypt-list-modes.md: « mcryptlistmodes
  - function.mcrypt-module-get-algo-block-size.md: mcryptmodulegetalgoblocksize »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcryptmoduleclose
---
# mcryptmoduleclose

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcryptmoduleclose — Закриває модуль mcrypt

**Увага**

Ця функція оголошена *Застарілої*, починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_module_close(resource $td): bool
```

Закриває цей обробник шифрування.

### Список параметрів

`td`

Дескриптор шифрування.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [mcryptmoduleopen()](function.mcrypt-module-open.md) - Відкриває модуль шифрування з використанням вказаних алгоритму та режиму
