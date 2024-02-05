---
navigation:
  - function.yaz-error.md: « yaz\_error
  - function.yaz-es.md: yaz\_es »
  - index.md: PHP Manual
  - ref.yaz.md: Функції YAZ
title: yaz\_es\_result
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# yaz\_es\_result

(PHP 4 >= 4.2.0, PECL yaz >= 0.9.0)

yaz\_es\_result — Перевіряє результат Extended Service

### Опис

```methodsynopsis
yaz_es_result(resource $id): array
```

Функція перевіряє останній повернутий сервером результат Extended Service. Extended Service ініціюється або за допомогою **yaz\_item\_order()**, або за допомогою [yaz\_es()](function.yaz-es.md)

### Список параметрів

`id`

Ідентифікатор підключення, що повертається [yaz\_connect()](function.yaz-connect.md)

### Значення, що повертаються

Повертає масив із елементом `targetReference` для посилання на операцію Extended Service (згенерованої та повернутої з сервера).

### Дивіться також

-   [yaz\_es()](function.yaz-es.md) \- готує Extended Service Request
