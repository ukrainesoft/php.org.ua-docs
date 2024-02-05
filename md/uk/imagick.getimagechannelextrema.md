---
navigation:
  - imagick.getimagechanneldistortions.md: '« Imagick::getImageChannelDistortions'
  - imagick.getimagechannelkurtosis.md: 'Imagick::getImageChannelKurtosis »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getImageChannelExtrema'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::getImageChannelExtrema

(PECL imagick 2, PECL imagick 3)

Imagick::getImageChannelExtrema — Повертає екстремуми для одного або кількох каналів зображення

**Увага**

Функція оголошена *застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::getImageChannelExtrema(int $channel): array
```

Отримує екстремуми для одного або кількох каналів зображення. Значення, що повертається - асоціативний масив з ключами "minima" і "maxima".

### Список параметрів

`channel`

Вкажіть будь-яку константу CHANNEL, яка підходить для вашого режиму каналу. Для використання більш ніж одного каналу об'єднайте константи типу CHANNEL за допомогою побітових операторів. Зверніться до цього списку [констант CHANNEL](imagick.constants.md#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.
