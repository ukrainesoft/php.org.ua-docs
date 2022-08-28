Видаляє краї із зображення

-   [« Gmagick::thumbnailimage](gmagick.thumbnailimage.html)
    
-   [Gmagick::write »](gmagick.write.html)
    
-   [PHP Manual](index.html)
    
-   [Gmagick](class.gmagick.html)
    
-   Видаляє краї із зображення
    

# Gmagick::trimimage

(PECL gmagick >= Unknown)

Gmagick::trimimage — Видаляє краї зображення

### Опис

```methodsynopsis
public Gmagick::trimimage(float $fuzz): Gmagick
```

Видаляє краї, які є кольором фону із зображенням.

### Список параметрів

`fuzz`

За замовчуванням ціль повинна точно відповідати певному кольору пікселя. Однак у багатьох випадках два кольори можуть трохи відрізнятися. Розмитий елемент зображення визначає, наскільки можна визначати, щоб два кольори вважалися однаковими. Параметр є зміною квантового діапазону.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.html)

### Помилки

Викликає **GmagickException** у разі виникнення помилки.