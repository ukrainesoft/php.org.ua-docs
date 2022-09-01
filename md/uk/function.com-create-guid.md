---
navigation:
  - ref.com.md: « Функции COM
  - function.com-event-sink.html: comeventsink »
  - index.md: PHP Manual
  - ref.com.md: Функции COM
title: comcreateguid
---
# comcreateguid

(PHP 5, PHP 7, PHP 8)

comcreateguid — створення унікального глобального ідентифікатора (GUID)

### Опис

```methodsynopsis
com_create_guid(): string|false
```

Створює унікальний глобальний ідентифікатор (GUID).

GUID генерується так само, як і DCE UUID, за винятком того, що, за конвенцією Microsoft, необхідно укладати GUID у фігурні дужки.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок з GUID або **`false`** у разі виникнення помилки.

### Дивіться також

-   **uuidcreate()** у модулі PECL uuid
