---
navigation:
  - function.openal-buffer-get.md: « openal\_buffer\_get
  - function.openal-context-create.md: openal\_context\_create »
  - index.md: PHP Manual
  - ref.openal.md: Функції OpenAL
title: openal\_buffer\_loadwav
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openal\_buffer\_loadwav

(PECL openal >= 0.1.0)

openal\_buffer\_loadwav — Завантажити файл у форматі wav у буфер

### Опис

```methodsynopsis
openal_buffer_loadwav(resource $buffer, string $wavfile): bool
```

### Список параметрів

`buffer`

Ресурс[Open AL(Buffer)](openal.resources.md) (раніше створений за допомогою [openal\_buffer\_create()](function.openal-buffer-create.md)

`wavfile`

Шлях до файлу .wav у файловій системі *local*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [openal\_buffer\_data()](function.openal-buffer-data.md) \- Завантаження буфера з даними
-   [openal\_stream()](function.openal-stream.md) \- Почати потокову передачу із джерела
