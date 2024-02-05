---
navigation:
  - function.openal-source-play.md: « openal\_source\_play
  - function.openal-source-set.md: openal\_source\_set »
  - index.md: PHP Manual
  - ref.openal.md: Функції OpenAL
title: openal\_source\_rewind
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openal\_source\_rewind

(PECL openal >= 0.1.0)

openal\_source\_rewind — Перемотати джерело на початок

### Опис

```methodsynopsis
openal_source_rewind(resource $source): bool
```

### Список параметрів

`source`

Ресурс[Open AL(Source)](openal.resources.md) (Створений раніше за допомогою [openal\_source\_create()](function.openal-source-create.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [openal\_source\_stop()](function.openal-source-stop.md) \- Зупинити відтворення джерела
-   [openal\_source\_pause()](function.openal-source-pause.md) \- Поставити джерело на паузу
-   [openal\_source\_play()](function.openal-source-play.md) \- Почати відтворення джерела
