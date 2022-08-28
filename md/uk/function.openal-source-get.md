Отримати властивість джерела OpenAL

-   [« openal\_source\_destroy](function.openal-source-destroy.html)
    
-   [openal\_source\_pause »](function.openal-source-pause.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenAL](ref.openal.html)
    
-   Отримати властивість джерела OpenAL
    

# openalsourceget

(PECL openal >= 0.1.0)

openalsourceget — Отримати властивість джерела OpenAL

### Опис

```methodsynopsis
openal_source_get(resource $source, int $property): mixed
```

### Список параметрів

`source`

Ресурс [Open AL(Source)](openal.resources.html) (Створений раніше за допомогою [openal\_source\_create()](function.openal-source-create.html)

`property`

Отримувана властивість, представлена ​​однією з констант: **`AL_SOURCE_RELATIVE`** (int), **`AL_SOURCE_STATE`** (int), **`AL_PITCH`** (float), **`AL_GAIN`** (float), **`AL_MIN_GAIN`** (float), **`AL_MAX_GAIN`** (float), **`AL_MAX_DISTANCE`** (float), **`AL_ROLLOFF_FACTOR`** (float), **`AL_CONE_OUTER_GAIN`** (float), **`AL_CONE_INNER_ANGLE`** (float), **`AL_CONE_OUTER_ANGLE`** (float), **`AL_REFERENCE_DISTANCE`** (float), **`AL_POSITION`** (array(float,float,float)), **`AL_VELOCITY`** (array(float,float,float)), **`AL_DIRECTION`** (array(float,float,float)).

### Значення, що повертаються

Повертає тип, пов'язаний із витягуваною властивістю або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openal\_source\_create()](function.openal-source-create.html) - Згенерувати джерело ресурсу
-   [openal\_source\_set()](function.openal-source-set.html) - Встановити властивість джерела
-   [openal\_source\_play()](function.openal-source-play.html) - Почати відтворення джерела