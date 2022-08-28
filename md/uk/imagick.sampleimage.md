Масштабує зображення з піксельною вибіркою

-   [« Imagick::roundCorners](imagick.roundcorners.html)
    
-   [Imagick::scaleImage »](imagick.scaleimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Масштабує зображення з піксельною вибіркою
    

# Imagick::sampleImage

(PECL imagick 2, PECL imagick 3)

Imagick::sampleImage — Масштабує зображення з піксельною вибіркою

### Опис

```methodsynopsis
public Imagick::sampleImage(int $columns, int $rows): bool
```

Масштабує зображення до бажаних розмірів за допомогою вибірки пікселів. На відміну від інших методів масштабування, цей метод не вводить додатковий колір у масштабоване зображення.

### Список параметрів

`columns`

`rows`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**