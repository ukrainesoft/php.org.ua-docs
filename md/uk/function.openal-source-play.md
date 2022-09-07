---
navigation:
  - function.openal-source-pause.md: « openalsourcepause
  - function.openal-source-rewind.md: openalsourcerewind »
  - index.md: PHP Manual
  - ref.openal.md: Функции OpenAL
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

Ресурс [Open AL(Source)](openal.resources.md) (Створений раніше за допомогою [openalsourcecreate()](function.openal-source-create.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openalsourcestop()](function.openal-source-stop.md) - Зупинити відтворення джерела
-   [openalsourcepause()](function.openal-source-pause.md) - Поставити джерело на паузу
-   [openalsourcerewind()](function.openal-source-rewind.md) - Перемотати джерело на початок
