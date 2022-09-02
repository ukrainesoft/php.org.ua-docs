---
navigation:
  - function.openal-buffer-data.md: « openalbufferdata
  - function.openal-buffer-get.md: openalbufferget »
  - index.md: PHP Manual
  - ref.openal.md: Функции OpenAL
title: openalbufferdestroy
---
# openalbufferdestroy

(PECL openal >= 0.1.0)

openalbufferdestroy — Знищує буфер OpenAL

### Опис

```methodsynopsis
openal_buffer_destroy(resource $buffer): bool
```

### Список параметрів

`buffer`

Ресурс [Open AL(Buffer)](openal.resources.md) (раніше створений за допомогою [openalbuffercreate()](function.openal-buffer-create.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openalbuffercreate()](function.openal-buffer-create.md) - Згенерувати буфер OpenAL
