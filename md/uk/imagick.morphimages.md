Перетворює набір зображень

-   [« Imagick::montageImage](imagick.montageimage.html)
    
-   [Imagick::morphology »](imagick.morphology.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Перетворює набір зображень
    

# Imagick::morphImages

(PECL imagick 2, PECL imagick 3)

Imagick::morphImages — Перетворює набір зображень

### Опис

```methodsynopsis
public Imagick::morphImages(int $number_frames): Imagick
```

Перетворює набір зображень. І пікселі зображення, і розмір лінійно інтерполуються, щоб створити видимість метаморфоз від одного зображення до іншого.

### Список параметрів

`number_frames`

Кількість проміжних зображень, що створюються.

### Значення, що повертаються

Метод повертає новий об'єкт Imagick у разі успішного виконання. Викликає **ImagickException** у разі виникнення помилки.