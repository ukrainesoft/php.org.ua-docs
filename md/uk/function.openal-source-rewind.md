---
navigation:
  - function.openal-source-play.html: « openalsourceplay
  - function.openal-source-set.html: openalsourceset »
  - index.md: PHP Manual
  - ref.openal.md: Функции OpenAL
title: openalsourcerewind
---
# openalsourcerewind

(PECL openal >= 0.1.0)

openalsourcerewind — Перемотати джерело на початок

### Опис

```methodsynopsis
openal_source_rewind(resource $source): bool
```

### Список параметрів

`source`

Ресурс [Open AL(Source)](openal.resources.md) (Створений раніше за допомогою [openalsourcecreate()](function.openal-source-create.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openalsourcestop()](function.openal-source-stop.html) - Зупинити відтворення джерела
-   [openalsourcepause()](function.openal-source-pause.html) - Поставити джерело на паузу
-   [openalsourceplay()](function.openal-source-play.html) - Почати відтворення джерела
