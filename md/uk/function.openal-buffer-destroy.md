---
navigation:
  - function.openal-buffer-data.md: « openal\_buffer\_data
  - function.openal-buffer-get.md: openal\_buffer\_get »
  - index.md: PHP Manual
  - ref.openal.md: Функції OpenAL
title: openal\_buffer\_destroy
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openal\_buffer\_destroy

(PECL openal >= 0.1.0)

openal\_buffer\_destroy — Знищує буфер OpenAL

### Опис

```methodsynopsis
openal_buffer_destroy(resource $buffer): bool
```

### Список параметрів

`buffer`

Ресурс[Open AL(Buffer)](openal.resources.md) (раніше створений за допомогою [openal\_buffer\_create()](function.openal-buffer-create.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [openal\_buffer\_create()](function.openal-buffer-create.md) \- Згенерувати буфер OpenAL
