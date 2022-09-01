---
navigation:
  - function.openal-source-pause.html: « openalsourcepause
  - function.openal-source-rewind.html: openalsourcerewind »
  - index.html: PHP Manual
  - ref.openal.html: Функции OpenAL
title: openalsourceplay
---
# openalsourceplay

(PECL openal >= 0.1.0)

openalsourceplay — Почати відтворення джерела

### Опис

```methodsynopsis
openal_source_play(resource $source): bool
```

### Список параметрів

`source`

Ресурс [Open AL(Source)](openal.resources.html) (Створений раніше за допомогою [openalsourcecreate()](function.openal-source-create.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openalsourcestop()](function.openal-source-stop.html) - Зупинити відтворення джерела
-   [openalsourcepause()](function.openal-source-pause.html) - Поставити джерело на паузу
-   [openalsourcerewind()](function.openal-source-rewind.html) - Перемотати джерело на початок
