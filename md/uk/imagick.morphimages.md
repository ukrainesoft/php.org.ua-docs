Перетворює набір зображень

-   [« Imagick::montageImage](imagick.montageimage.md)
    
-   [Imagick::morphology »](imagick.morphology.md)
    
-   [PHP Manual](index.md)
    
-   [Imagick](class.imagick.md)
    
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