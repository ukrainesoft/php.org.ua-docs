---
navigation:
  - function.openal-buffer-destroy.md: « openal\_buffer\_destroy
  - function.openal-buffer-loadwav.md: openal\_buffer\_loadwav »
  - index.md: PHP Manual
  - ref.openal.md: Функції OpenAL
title: openal\_buffer\_get
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openal\_buffer\_get

(PECL openal >= 0.1.0)

openal\_buffer\_get — Отримати властивість буфера OpenAL

### Опис

```methodsynopsis
openal_buffer_get(resource $buffer, int $property): int|false
```

### Список параметрів

`buffer`

Ресурс[Open AL(Buffer)](openal.resources.md) (Створений раніше за допомогою [openal\_buffer\_create()](function.openal-buffer-create.md)

`property`

Одна з властивостей, задана у вигляді константи: **`AL_FREQUENCY`** **`AL_BITS`** **`AL_CHANNELS`** і **`AL_SIZE`**

### Значення, що повертаються

Повертає ціле значення, що відповідає запрошеному властивості `property`или\*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [openal\_buffer\_create()](function.openal-buffer-create.md) \- Згенерувати буфер OpenAL
