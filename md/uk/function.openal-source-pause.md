---
navigation:
  - function.openal-source-get.html: « openalsourceget
  - function.openal-source-play.html: openalsourceplay »
  - index.md: PHP Manual
  - ref.openal.md: Функции OpenAL
title: openalsourcepause
---
# openalsourcepause

(PECL openal >= 0.1.0)

openalsourcepause — Поставити джерело на паузу

### Опис

```methodsynopsis
openal_source_pause(resource $source): bool
```

### Список параметрів

`source`

Ресурс [Open AL(Source)](openal.resources.md) (Створений раніше за допомогою [openalsourcecreate()](function.openal-source-create.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openalsourcestop()](function.openal-source-stop.md) - Зупинити відтворення джерела
-   [openalsourceplay()](function.openal-source-play.md) - Почати відтворення джерела
-   [openalsourcerewind()](function.openal-source-rewind.md) - Перемотати джерело на початок
