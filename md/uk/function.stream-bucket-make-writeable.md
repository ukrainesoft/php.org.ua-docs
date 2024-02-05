---
navigation:
  - function.stream-bucket-append.md: « stream\_bucket\_append
  - function.stream-bucket-new.md: stream\_bucket\_new »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_bucket\_make\_writeable
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_bucket\_make\_writeable

(PHP 5, PHP 7, PHP 8)

stream\_bucket\_make\_writeable — Повертає об'єкт бакета із бригади для подальшої роботи з ним

### Опис

```methodsynopsis
stream_bucket_make_writeable(resource $brigade): ?object
```

Функція викликається щоразу, коли виникає необхідність у доступі до вмісту, що міститься в бригаді та роботі з ним. Зазвичай функція викликається з методу [php\_user\_filter::filter()](php-user-filter.filter.md)

### Список параметрів

`brigade`

Бригада, з якої необхідно повернути об'єкт бакета.

### Значення, що повертаються

Повертає об'єкт бакета з властивостями, наведеними нижче або **`null`**

data (string)

`data` `bucket` Поточний рядок у бакет.

datalen (integer)

`datalen` `bucket`Длина строки в бакете.

### Дивіться також

-   [stream\_bucket\_append()](function.stream-bucket-append.md) \- Додати бакет до бригади
-   [stream\_bucket\_prepend()](function.stream-bucket-prepend.md) \- Додає бакет на початок бригади
