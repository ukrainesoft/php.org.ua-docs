---
navigation:
  - function.yaz-es.md: « yaz\_es
  - function.yaz-hits.md: yaz\_hits »
  - index.md: PHP Manual
  - ref.yaz.md: Функції YAZ
title: yaz\_get\_option
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# yaz\_get\_option

(PECL yaz >= 0.9.0)

yaz\_get\_option — Повертає значення параметра для підключення

### Опис

```methodsynopsis
yaz_get_option(resource $id, string $name): string
```

Повертає значення параметра, вказаного в `name`

### Список параметрів

`id`

Ресурс підключення, що повертається [yaz\_connect()](function.yaz-connect.md)

`name`

Назву параметра.

### Значення, що повертаються

Повертає значення вказаної опції або порожній рядок, якщо опцію не було встановлено.

### Дивіться також

-   Опис[yaz\_set\_option()](function.yaz-set-option.md) \- Встановлює параметри з'єднання для перегляду доступних параметрів
