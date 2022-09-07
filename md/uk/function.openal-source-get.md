---
navigation:
  - function.openal-source-destroy.md: « openalsourcedestroy
  - function.openal-source-pause.md: openalsourcepause »
  - index.md: PHP Manual
  - ref.openal.md: Функции OpenAL
title: openalsourceget
---
# openalsourceget

(PECL openal >= 0.1.0)

openalsourceget — Отримати властивість джерела OpenAL

### Опис

```methodsynopsis
openal_source_get(resource $source, int $property): mixed
```

### Список параметрів

`source`

Ресурс [Open AL(Source)](openal.resources.md) (Створений раніше за допомогою [openalsourcecreate()](function.openal-source-create.md)

`property`

Отримувана властивість, представлена ​​однією з констант: **`AL_SOURCE_RELATIVE`** (int), **`AL_SOURCE_STATE`** (int), **`AL_PITCH`** (float), **`AL_GAIN`** (float), **`AL_MIN_GAIN`** (float), **`AL_MAX_GAIN`** (float), **`AL_MAX_DISTANCE`** (float), **`AL_ROLLOFF_FACTOR`** (float), **`AL_CONE_OUTER_GAIN`** (float), **`AL_CONE_INNER_ANGLE`** (float), **`AL_CONE_OUTER_ANGLE`** (float), **`AL_REFERENCE_DISTANCE`** (float), **`AL_POSITION`** (array(float,float,float)), **`AL_VELOCITY`** (array(float,float,float)), **`AL_DIRECTION`** (array(float,float,float)).

### Значення, що повертаються

Повертає тип, пов'язаний із витягуваною властивістю або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openalsourcecreate()](function.openal-source-create.md) - Згенерувати джерело ресурсу
-   [openalsourceset()](function.openal-source-set.md) - Встановити властивість джерела
-   [openalsourceplay()](function.openal-source-play.md) - Почати відтворення джерела
