---
navigation:
  - function.openal-source-destroy.md: « openal\_source\_destroy
  - function.openal-source-pause.md: openal\_source\_pause »
  - index.md: PHP Manual
  - ref.openal.md: Функції OpenAL
title: openal\_source\_get
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openal\_source\_get

(PECL openal >= 0.1.0)

openal\_source\_get — Отримати властивість джерела OpenAL

### Опис

```methodsynopsis
openal_source_get(resource $source, int $property): mixed
```

### Список параметрів

`source`

Ресурс[Open AL(Source)](openal.resources.md) (Створений раніше за допомогою [openal\_source\_create()](function.openal-source-create.md)

`property`

Получаемое свойство, представленное одной из констант:**`AL_SOURCE_RELATIVE`**(int),**`AL_SOURCE_STATE`**(int),**`AL_PITCH`**(float),**`AL_GAIN`**(float),**`AL_MIN_GAIN`**(float),**`AL_MAX_GAIN`**(float),**`AL_MAX_DISTANCE`**(float),**`AL_ROLLOFF_FACTOR`**(float),**`AL_CONE_OUTER_GAIN`**(float),**`AL_CONE_INNER_ANGLE`**(float),**`AL_CONE_OUTER_ANGLE`**(float),**`AL_REFERENCE_DISTANCE`**(float),**`AL_POSITION`**(array(float,float,float)),**`AL_VELOCITY`**(array(float,float,float)),**`AL_DIRECTION`**(array(float,float,float)).

### Значення, що повертаються

Повертає тип, пов'язаний із витягуваною властивістю або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [openal\_source\_create()](function.openal-source-create.md) \- Згенерувати джерело ресурсу
-   [openal\_source\_set()](function.openal-source-set.md) \- Встановити властивість джерела
-   [openal\_source\_play()](function.openal-source-play.md) \- Почати відтворення джерела
