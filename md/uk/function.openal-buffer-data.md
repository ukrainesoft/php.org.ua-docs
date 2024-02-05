---
navigation:
  - function.openal-buffer-create.md: « openal\_buffer\_create
  - function.openal-buffer-destroy.md: openal\_buffer\_destroy »
  - index.md: PHP Manual
  - ref.openal.md: Функції OpenAL
title: openal\_buffer\_data
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openal\_buffer\_data

(PECL openal >= 0.1.0)

openal\_buffer\_data — Завантаження буфера з даними

### Опис

```methodsynopsis
openal_buffer_data(    resource $buffer,    int $format,    string $data,    int $freq): bool
```

### Список параметрів

`buffer`

Ресурс[Open AL(Buffer)](openal.resources.md) (Створений раніше за допомогою [openal\_buffer\_create()](function.openal-buffer-create.md)

`format`

Формат`data`, представлений однією з констант: **`AL_FORMAT_MONO8`** **`AL_FORMAT_MONO16`** **`AL_FORMAT_STEREO8`** і **`AL_FORMAT_STEREO16`**

`data`

Блок двійкових аудіоданих у вказаному форматі `format` та з частотою `freq`

`freq`

Частота`data`, Задана в герцах.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [openal\_buffer\_loadwav()](function.openal-buffer-loadwav.md) \- Завантажити файл у форматі wav у буфер
-   [openal\_stream()](function.openal-stream.md) \- Почати потокову передачу із джерела
