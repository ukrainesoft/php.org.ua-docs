---
navigation:
  - function.openal-listener-get.md: « openal\_listener\_get
  - function.openal-source-create.md: openal\_source\_create »
  - index.md: PHP Manual
  - ref.openal.md: Функції OpenAL
title: openal\_listener\_set
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openal\_listener\_set

(PECL openal >= 0.1.0)

openal\_listener\_set — Встановлення якості прослуховувача

### Опис

```methodsynopsis
openal_listener_set(int $property, mixed $setting): bool
```

### Список параметрів

`property`

Устанавливаемое свойство, представленное одной из констант:**`AL_GAIN`**(float),**`AL_POSITION`**(array(float,float,float)),**`AL_VELOCITY`**(array(float,float,float)) и\*\*`AL_ORIENTATION`\*\*(array(float,float,float)).

`setting`

Значення для установки, або число з точкою, що плаває, або масив з числами з плаваючими точками.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [openal\_listener\_get()](function.openal-listener-get.md) \- Отримати властивість прослуховувача
