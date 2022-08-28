Імітує розмиття під час руху

-   [« Gmagick::modulateimage](gmagick.modulateimage.html)
    
-   [Gmagick::newimage »](gmagick.newimage.html)
    
-   [PHP Manual](index.html)
    
-   [Gmagick](class.gmagick.html)
    
-   Імітує розмиття під час руху
    

# Gmagick::motionblurimage

(PECL gmagick >= Unknown)

Gmagick::motionblurimage — Імітує розмиття під час руху

### Опис

```methodsynopsis
public Gmagick::motionblurimage(float $radius, float $sigma, float $angle): Gmagick
```

Імітує розмиття під час руху. Згортає зображення за допомогою гаусівського оператора заданого радіусу та стандартного відхилення (sigma). Для отримання прийнятних результатів radius повинен бути більшим за sigma. При використанні значення radius, що дорівнює 0, **Gmagick::motionblurimage()** вибере вам відповідний радіус. Параметр angle задає кут розмиття руху.

### Список параметрів

`radius`

Радіус у пікселях, крім центрального пікселя.

`sigma`

Стандартне відхилення у пікселях.

`angle`

Кут, під яким застосовується ефект.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.html) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.