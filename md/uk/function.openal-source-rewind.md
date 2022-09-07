---
navigation:
  - function.openal-source-play.md: « openalsourceplay
  - function.openal-source-set.md: openalsourceset »
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

Ресурс [Open AL(Source)](openal.resources.md) (Створений раніше за допомогою [openalsourcecreate()](function.openal-source-create.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openalsourcestop()](function.openal-source-stop.md) - Зупинити відтворення джерела
-   [openalsourcepause()](function.openal-source-pause.md) - Поставити джерело на паузу
-   [openalsourceplay()](function.openal-source-play.md) - Почати відтворення джерела
