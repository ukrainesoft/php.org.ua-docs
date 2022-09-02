---
navigation:
  - function.yaz-es.md: « yazес
  - function.yaz-hits.md: yazhits »
  - index.md: PHP Manual
  - ref.yaz.md: Функции YAZ
title: yazgetoption
---
# yazgetoption

(PECL yaz >= 0.9.0)

yazgetoption — Повертає значення параметра для підключення

### Опис

```methodsynopsis
yaz_get_option(resource $id, string $name): string
```

Повертає значення параметра, вказаного в `name`

### Список параметрів

`id`

Ресурс підключення, що повертається [yazconnect()](function.yaz-connect.md)

`name`

Назву параметра.

### Значення, що повертаються

Повертає значення вказаної опції або порожній рядок, якщо опцію не було встановлено.

### Дивіться також

-   Опис [yazsetoption()](function.yaz-set-option.md) - Встановлює параметри з'єднання для перегляду доступних параметрів
