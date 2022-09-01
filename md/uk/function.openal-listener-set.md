---
navigation:
  - function.openal-listener-get.html: « openallistenerget
  - function.openal-source-create.html: openalsourcecreate »
  - index.md: PHP Manual
  - ref.openal.md: Функции OpenAL
title: openallistenerset
---
# openallistenerset

(PECL openal >= 0.1.0)

openallistenerset — Встановлення якості прослуховувача

### Опис

```methodsynopsis
openal_listener_set(int $property, mixed $setting): bool
```

### Список параметрів

`property`

Встановлювана властивість, представлена ​​однією з констант: **`AL_GAIN`** (float), **`AL_POSITION`** (array(float,float,float)), **`AL_VELOCITY`** (array(float,float,float)) та **`AL_ORIENTATION`** (array(float,float,float)).

`setting`

Значення для установки або число з плаваючою точкою або масив з числами з плаваючими точками.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openallistenerget()](function.openal-listener-get.html) - Отримати властивість прослуховувача
