---
navigation:
  - function.ob-get-length.md: « ob\_get\_length
  - function.ob-get-status.md: ob\_get\_status »
  - index.md: PHP Manual
  - ref.outcontrol.md: Функції контролю виведення
title: ob\_get\_level
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ob\_get\_level

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

ob\_get\_level - Повертає рівень вкладеності механізму буферизації виводу

### Опис

```methodsynopsis
ob_get_level(): int
```

Повертає рівень вкладеності механізму буферизації виведення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рівень вкладеності обробників буферизації виводу або 0, якщо не активна буферизація.

**Застереження**

Функції \*\*ob\_get\_level()\*\*и[ob\_get\_status()](function.ob-get-status.md) по-різному оцінюють той самий рівень вкладеності; значення відхилено на одиницю. Для функції **ob\_get\_level()** перший рівень - це . Тоді як для функції [ob\_get\_status()](function.ob-get-status.md) перший рівень - це

### Дивіться також

-   [ob\_start()](function.ob-start.md) \- Включає буферизацію виводу
-   [ob\_get\_status()](function.ob-get-status.md) \- набуває статусу буфера виводу
-   [ob\_get\_contents()](function.ob-get-contents.md) \- Повертає вміст буфера виводу
