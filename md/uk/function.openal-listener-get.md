---
navigation:
  - function.openal-device-open.md: « openal\_device\_open
  - function.openal-listener-set.md: openal\_listener\_set »
  - index.md: PHP Manual
  - ref.openal.md: Функції OpenAL
title: openal\_listener\_get
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openal\_listener\_get

(PECL openal >= 0.1.0)

openal\_listener\_get — Отримати властивість прослуховувача

### Опис

```methodsynopsis
openal_listener_get(int $property): mixed
```

### Список параметрів

`property`

Запрашиваемое свойство, представленное одной из констант:**`AL_GAIN`**(float),**`AL_POSITION`**(array(float,float,float)),**`AL_VELOCITY`**(array(float,float,float)) и\*\*`AL_ORIENTATION`\*\*(array(float,float,float)).

### Значення, що повертаються

Повертає число з плаваючою точкою або масив чисел з плаваючими точками (при необхідності) або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [openal\_listener\_set()](function.openal-listener-set.md) \- Встановлення якості прослуховувача
