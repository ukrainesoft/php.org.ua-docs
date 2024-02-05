---
navigation:
  - function.openal-source-rewind.md: « openal\_source\_rewind
  - function.openal-source-stop.md: openal\_source\_stop »
  - index.md: PHP Manual
  - ref.openal.md: Функції OpenAL
title: openal\_source\_set
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openal\_source\_set

(PECL openal >= 0.1.0)

openal\_source\_set — Встановити властивість джерела

### Опис

```methodsynopsis
openal_source_set(resource $source, int $property, mixed $setting): bool
```

### Список параметрів

`source`

Ресурс[Open AL(Source)](openal.resources.md) (Створений раніше за допомогою [openal\_source\_create()](function.openal-source-create.md)

`property`

Устанавливаемое свойство, представляющее одну из констант:**`AL_BUFFER`** (OpenAL (джерело)), **`AL_LOOPING`**(bool),**`AL_SOURCE_RELATIVE`**(int),**`AL_SOURCE_STATE`**(int),**`AL_PITCH`**(float),**`AL_GAIN`**(float),**`AL_MIN_GAIN`**(float),**`AL_MAX_GAIN`**(float),**`AL_MAX_DISTANCE`**(float),**`AL_ROLLOFF_FACTOR`**(float),**`AL_CONE_OUTER_GAIN`**(float),**`AL_CONE_INNER_ANGLE`**(float),**`AL_CONE_OUTER_ANGLE`**(float),**`AL_REFERENCE_DISTANCE`**(float),**`AL_POSITION`**(array(float,float,float)),**`AL_VELOCITY`**(array(float,float,float)),**`AL_DIRECTION`**(array(float,float,float)).

`setting`

Значение для присвоения указанному свойству`property`Обратитесь к описанию параметра`property` для опису очікуваних параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [openal\_source\_create()](function.openal-source-create.md) \- Згенерувати джерело ресурсу
-   [openal\_source\_get()](function.openal-source-get.md) \- Отримати властивість джерела OpenAL
-   [openal\_source\_play()](function.openal-source-play.md) \- Почати відтворення джерела
