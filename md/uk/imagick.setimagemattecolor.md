Встановлює матовий колір зображення

-   [« Imagick::setImageMatte](imagick.setimagematte.html)
    
-   [Imagick::setImageOpacity »](imagick.setimageopacity.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Встановлює матовий колір зображення
    

# Imagick::setImageMatteColor

(PECL imagick 2, PECL imagick 3)

Imagick::setImageMatteColor — Встановлює матовий колір зображення

**Увага**

Функція оголошена *застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::setImageMatteColor(mixed $matte): bool
```

Встановлює матовий колір зображення.

### Список параметрів

`matte`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| PECL imagick 2.1.0 | Тепер дозволяє використовувати рядок, що представляє колір, як параметр. Попередні версії дозволяли використовувати лише об'єкт ImagickPixel. |