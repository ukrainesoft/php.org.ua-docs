Застосовує ефект соляризації до зображення

-   [« Gmagick::shearimage](gmagick.shearimage.html)
    
-   [Gmagick::spreadimage »](gmagick.spreadimage.html)
    
-   [PHP Manual](index.html)
    
-   [Gmagick](class.gmagick.html)
    
-   Застосовує ефект соляризації до зображення
    

# Gmagick::solarizeimage

(PECL gmagick >= Unknown)

Gmagick::solarizeimage — Застосовує ефект соляризації до зображення.

### Опис

```methodsynopsis
public Gmagick::solarizeimage(int $threshold): Gmagick
```

Застосовує особливий ефект до зображення, подібний до ефекту, що досягається у фотолабораторії за допомогою вибіркового експонування областей світлочутливого паперу на світ. Поріг варіюється від 0 до QuantumRange і є мірою соляризації.

### Список параметрів

`threshold`

Ступінь соляризації.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.html) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.