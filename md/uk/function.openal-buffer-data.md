---
navigation:
  - function.openal-buffer-create.md: « openalbuffercreate
  - function.openal-buffer-destroy.md: openalbufferdestroy »
  - index.md: PHP Manual
  - ref.openal.md: Функции OpenAL
title: openalbufferdata
---
# openalbufferdata

(PECL openal >= 0.1.0)

openalbufferdata — Завантаження буфера з даними

### Опис

```methodsynopsis
openal_buffer_data(    resource $buffer,    int $format,    string $data,    int $freq): bool
```

### Список параметрів

`buffer`

Ресурс [Open AL(Buffer)](openal.resources.md) (Створений раніше за допомогою [openalbuffercreate()](function.openal-buffer-create.md)

`format`

Формат `data`, представлений однією з констант: **`AL_FORMAT_MONO8`** **`AL_FORMAT_MONO16`** **`AL_FORMAT_STEREO8`** і **`AL_FORMAT_STEREO16`**

`data`

Блок двійкових аудіоданих у вказаному форматі `format` та з частотою `freq`

`freq`

Частота `data`, Задана в герцах.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openalbufferloadwav()](function.openal-buffer-loadwav.md) - Завантажити файл у форматі wav у буфер
-   [openalstream()](function.openal-stream.md) - Почати потокову передачу із джерела
