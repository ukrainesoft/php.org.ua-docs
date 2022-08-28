Повертає артефакт зображення

-   [« Imagick::getImageAlphaChannel](imagick.getimagealphachannel.html)
    
-   [Imagick::getImageAttribute »](imagick.getimageattribute.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Повертає артефакт зображення
    

# Imagick::getImageArtifact

(PECL imagick 3)

Imagick::getImageArtifact — Повертає артефакт зображення

### Опис

```methodsynopsis
public Imagick::getImageArtifact(string $artifact): string
```

Повертає артефакт, пов'язаний із зображенням. Різниця між властивостями зображення та артефактами зображення полягає в тому, що властивості є загальнодоступними, а артефакти – закритими.

### Список параметрів

`artifact`

Ім'я артефакту.

### Значення, що повертаються

Повертає значення артефакту у разі успішного виконання.

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Дивіться також

-   [Imagick::setImageArtifact()](imagick.setimageartifact.html) - Встановлює артефакт зображення
-   [Imagick::deleteImageArtifact()](imagick.deleteimageartifact.html) - Видаляє артефакт зображення