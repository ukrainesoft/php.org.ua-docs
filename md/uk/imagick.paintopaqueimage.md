Змінює будь-який піксель, що відповідає кольору

-   [« Imagick::paintFloodfillImage](imagick.paintfloodfillimage.html)
    
-   [Imagick::paintTransparentImage »](imagick.painttransparentimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Змінює будь-який піксель, що відповідає кольору
    

# Imagick::paintOpaqueImage

(PECL imagick 2, PECL imagick 3)

Imagick::paintOpaqueImage — Змінює будь-який піксель, що відповідає кольору

**Увага**

Функція оголошена *застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::paintOpaqueImage(    mixed $target,    mixed $fill,    float $fuzz,    int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Змінює будь-який піксель, який відповідає кольору, на колір, визначений заливкою.

### Список параметрів

`target`

Змінює цільовий колір на колір заливки зображення. Об'єкт ImagickPixel або рядок, який представляє цільовий колір.

`fill`

Об'єкт ImagickPixel або рядок, який представляє колір заливки.

`fuzz`

Міра округлення (fuzz) зображення визначає, наскільки прийнятно розглядати два кольори як і той самий.

`channel`

Вкажіть будь-яку константу каналу, яка відповідає режиму каналу. Щоб застосувати більше одного каналу, об'єднайте константи типу каналу за допомогою побітових операторів. Зверніться до цього списку [констант канала](imagick.constants.html#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| PECL imagick 2.1.0 | Тепер допускається передавати рядок, що представляє колір, перший і другий параметр. Попередні версії допускали лише об'єкт ImagickPixel. |