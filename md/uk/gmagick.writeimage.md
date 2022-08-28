Записує зображення у вказаний файл

-   [« Gmagick::write](gmagick.write.html)
    
-   [GmagickDraw »](class.gmagickdraw.html)
    
-   [PHP Manual](index.html)
    
-   [Gmagick](class.gmagick.html)
    
-   Записує зображення у вказаний файл
    

# Gmagick::writeimage

(PECL gmagick >= Unknown)

Gmagick::writeimage — Записує зображення у вказаний файл

### Опис

```methodsynopsis
public Gmagick::writeimage(string $filename, bool $all_frames = false): Gmagick
```

Записує зображення у вказаний файл. Якщо в якості імені файлу вказано **`null`**, то зображення буде записано у файл, заданий [Gmagick::readimage()](gmagick.readimage.html) або [Gmagick::setimagefilename()](gmagick.setimagefilename.html)

### Список параметрів

`filename`

Ім'я файлу.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.html)

### Помилки

Викликає **GmagickException** у разі виникнення помилки.