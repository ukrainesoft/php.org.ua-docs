---
navigation:
  - function.mcrypt-list-modes.md: « mcrypt\_list\_modes
  - function.mcrypt-module-get-algo-block-size.md: mcrypt\_module\_get\_algo\_block\_size »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcrypt\_module\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mcrypt\_module\_close

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcrypt\_module\_close — Закриває модуль mcrypt

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_module_close(resource $td): bool
```

Закриває цей обробник шифрування.

### Список параметрів

`td`

Дескриптор шифрування.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [mcrypt\_module\_open()](function.mcrypt-module-open.md) \- Відкриває модуль шифрування з використанням вказаних алгоритму та режиму
