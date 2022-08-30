Створює імітацію ефекту тривимірної кнопки

-   [« Gmagick::radialblurimage](gmagick.radialblurimage.md)
    
-   [Gmagick::read »](gmagick.read.md)
    
-   [PHP Manual](index.md)
    
-   [Gmagick](class.gmagick.md)
    
-   Створює імітацію ефекту тривимірної кнопки
    

# Gmagick::raiseimage

(PECL gmagick >= Unknown)

Gmagick::raiseimage — Створює імітацію ефекту тривимірної кнопки

### Опис

```methodsynopsis
public Gmagick::raiseimage(    int $width,    int $height,    int $x,    int $y,    bool $raise): Gmagick
```

Створює імітацію ефекту тривимірної кнопки, освітлюючи та затемнюючи краї зображення. Ширина та висота елементів raiseinfo визначають ширину вертикального та горизонтального краю ефекту.

### Список параметрів

`width`

Ширина області, яку необхідно підняти.

`height`

Висота площі, що піднімається.

`x`

Координати X.

`y`

Координата Y.

`raise`

Значення, відмінне від нуля, створює ефект тривимірного підвищення, інакше - ефект зниження.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.