---
navigation:
  - function.openal-buffer-get.md: « openalbufferget
  - function.openal-context-create.md: openalcontextcreate »
  - index.md: PHP Manual
  - ref.openal.md: Функции OpenAL
title: openalbufferloadwav
---
# openalbufferloadwav

(PECL openal >= 0.1.0)

openalbufferloadwav — Завантажити файл у форматі wav у буфер

### Опис

```methodsynopsis
openal_buffer_loadwav(resource $buffer, string $wavfile): bool
```

### Список параметрів

`buffer`

Ресурс [Open AL(Buffer)](openal.resources.md) (раніше створений за допомогою [openalbuffercreate()](function.openal-buffer-create.md)

`wavfile`

Шлях до файлу .wav у файловій системі *local*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openalbufferdata()](function.openal-buffer-data.md) - Завантаження буфера з даними
-   [openalstream()](function.openal-stream.md) - Почати потокову передачу із джерела
