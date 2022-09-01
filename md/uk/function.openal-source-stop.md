---
navigation:
  - function.openal-source-set.html: « openalsourceset
  - function.openal-stream.html: openalstream »
  - index.md: PHP Manual
  - ref.openal.md: Функции OpenAL
title: openalsourcestop
---
# openalsourcestop

(PECL openal >= 0.1.0)

openalsourcestop — Зупинити відтворення джерела

### Опис

```methodsynopsis
openal_source_stop(resource $source): bool
```

### Список параметрів

`source`

Ресурс [Open AL(Source)](openal.resources.md) (Створений раніше за допомогою [openalsourcecreate()](function.openal-source-create.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openalsourceplay()](function.openal-source-play.md) - Почати відтворення джерела
-   [openalsourcepause()](function.openal-source-pause.md) - Поставити джерело на паузу
-   [openalsourcerewind()](function.openal-source-rewind.md) - Перемотати джерело на початок
