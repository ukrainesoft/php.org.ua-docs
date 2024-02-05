---
navigation:
  - ref.com.md: « Функції COM
  - function.com-event-sink.md: com\_event\_sink »
  - index.md: PHP Manual
  - ref.com.md: Функції COM
title: com\_create\_guid
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# com\_create\_guid

(PHP 5, PHP 7, PHP 8)

com\_create\_guid — створення унікального глобального ідентифікатора (GUID)

### Опис

```methodsynopsis
com_create_guid(): string|false
```

Створює унікальний глобальний ідентифікатор (GUID).

GUID генерується так само як і DCE UUID, за винятком того, що за конвенцією Microsoft необхідно укладати GUID у фігурні дужки.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок з GUID або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   \*\*uuid\_create()\*\*у модулі PECL uuid
