---
navigation:
  - function.yaz-error.html: « yazerror
  - function.yaz-es.html: yazes »
  - index.html: PHP Manual
  - ref.yaz.html: Функции YAZ
title: yazесresult
---
# yazесresult

(PHP 4> = 4.2.0, PECL yaz> = 0.9.0)

yazесresult — Перевіряє результат Extended Service

### Опис

```methodsynopsis
yaz_es_result(resource $id): array
```

Функція перевіряє останній повернутий сервером результат Extended Service. Extended Service ініціюється або за допомогою **yazitemorder()**, або за допомогою [yazes()](function.yaz-es.md)

### Список параметрів

`id`

Ідентифікатор підключення, що повертається [yazconnect()](function.yaz-connect.md)

### Значення, що повертаються

Повертає масив із елементом `targetReference` для посилання на операцію Extended Service (згенерованої та повернутої з сервера).

### Дивіться також

-   [yazes()](function.yaz-es.md) - готує Extended Service Request
