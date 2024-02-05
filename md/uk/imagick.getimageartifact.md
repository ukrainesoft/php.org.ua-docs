---
navigation:
  - imagick.getimagealphachannel.md: '« Imagick::getImageAlphaChannel'
  - imagick.getimageattribute.md: 'Imagick::getImageAttribute »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getImageArtifact'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

-   [Imagick::setImageArtifact()](imagick.setimageartifact.md) \- Встановлює артефакт зображення
-   [Imagick::deleteImageArtifact()](imagick.deleteimageartifact.md) \- Видаляє артефакт зображення
