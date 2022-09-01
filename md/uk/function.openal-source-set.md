---
navigation:
  - function.openal-source-rewind.html: « openalsourcerewind
  - function.openal-source-stop.html: openalsourcestop »
  - index.md: PHP Manual
  - ref.openal.md: Функции OpenAL
title: openalsourceset
---
# openalsourceset

(PECL openal >= 0.1.0)

openalsourceset — Встановити властивість джерела

### Опис

```methodsynopsis
openal_source_set(resource $source, int $property, mixed $setting): bool
```

### Список параметрів

`source`

Ресурс [Open AL(Source)](openal.resources.md) (Створений раніше за допомогою [openalsourcecreate()](function.openal-source-create.md)

`property`

Встановлювана властивість, що представляє одну з констант: **`AL_BUFFER`** (OpenAL (джерело)), **`AL_LOOPING`** (bool), **`AL_SOURCE_RELATIVE`** (int), **`AL_SOURCE_STATE`** (int), **`AL_PITCH`** (float), **`AL_GAIN`** (float), **`AL_MIN_GAIN`** (float), **`AL_MAX_GAIN`** (float), **`AL_MAX_DISTANCE`** (float), **`AL_ROLLOFF_FACTOR`** (float), **`AL_CONE_OUTER_GAIN`** (float), **`AL_CONE_INNER_ANGLE`** (float), **`AL_CONE_OUTER_ANGLE`** (float), **`AL_REFERENCE_DISTANCE`** (float), **`AL_POSITION`** (array(float,float,float)), **`AL_VELOCITY`** (array(float,float,float)), **`AL_DIRECTION`** (array(float,float,float)).

`setting`

Значення для присвоєння зазначеній властивості `property`. Зверніться до опису параметра `property` для опису очікуваних параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openalsourcecreate()](function.openal-source-create.md) - Згенерувати джерело ресурсу
-   [openalsourceget()](function.openal-source-get.md) - Отримати властивість джерела OpenAL
-   [openalsourceplay()](function.openal-source-play.md) - Почати відтворення джерела
