---
navigation:
  - function.openal-device-open.html: « openaldeviceopen
  - function.openal-listener-set.html: openallistenerset »
  - index.md: PHP Manual
  - ref.openal.md: Функции OpenAL
title: openallistenerget
---
# openallistenerget

(PECL openal >= 0.1.0)

openallistenerget — Отримати властивість прослуховувача

### Опис

```methodsynopsis
openal_listener_get(int $property): mixed
```

### Список параметрів

`property`

Запитувана властивість, представлена ​​однією з констант: **`AL_GAIN`** (float), **`AL_POSITION`** (array(float,float,float)), **`AL_VELOCITY`** (array(float,float,float)) та **`AL_ORIENTATION`** (array(float,float,float)).

### Значення, що повертаються

Повертає число з плаваючою точкою або масив чисел з плаваючими точками (при необхідності) або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openallistenerset()](function.openal-listener-set.html) - Встановлення якості прослуховувача
