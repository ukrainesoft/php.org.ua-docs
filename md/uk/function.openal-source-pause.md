---
navigation:
  - function.openal-source-get.md: « openal\_source\_get
  - function.openal-source-play.md: openal\_source\_play »
  - index.md: PHP Manual
  - ref.openal.md: Функції OpenAL
title: openal\_source\_pause
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openal\_source\_pause

(PECL openal >= 0.1.0)

openal\_source\_pause — Поставити джерело на паузу

### Опис

```methodsynopsis
openal_source_pause(resource $source): bool
```

### Список параметрів

`source`

Ресурс[Open AL(Source)](openal.resources.md) (Створений раніше за допомогою [openal\_source\_create()](function.openal-source-create.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [openal\_source\_stop()](function.openal-source-stop.md) \- Зупинити відтворення джерела
-   [openal\_source\_play()](function.openal-source-play.md) \- Почати відтворення джерела
-   [openal\_source\_rewind()](function.openal-source-rewind.md) \- Перемотати джерело на початок
