---
navigation:
  - imagick.getimagechanneldistortions.html: '« Imagick::getImageChannelDistortions'
  - imagick.getimagechannelkurtosis.html: 'Imagick::getImageChannelKurtosis »'
  - index.html: PHP Manual
  - class.imagick.html: Imagick
title: 'Imagick::getImageChannelExtrema'
---
# Imagick::getImageChannelExtrema

(PECL imagick 2, PECL imagick 3)

Imagick::getImageChannelExtrema — Повертає екстремуми для одного або кількох каналів зображення

**Увага**

Функція оголошена *Застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::getImageChannelExtrema(int $channel): array
```

Отримує екстремуми для одного або кількох каналів зображення. Значення, що повертається - асоціативний масив з ключами "minima" і "maxima".

### Список параметрів

`channel`

Вкажіть будь-яку константу CHANNEL, яка підходить для вашого режиму каналу. Для використання більш ніж одного каналу об'єднайте константи типу CHANNEL за допомогою побітових операторів. Зверніться до цього списку [констант CHANNEL](imagick.constants.html#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.
