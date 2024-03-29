---
navigation:
  - imagick.deconstructimages.md: '« Imagick::deconstructImages'
  - imagick.deleteimageproperty.md: 'Imagick::deleteImageProperty »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::deleteImageArtifact'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::deleteImageArtifact

(PECL imagick 3)

Imagick::deleteImageArtifact — Видаляє артефакт зображення

### Опис

```methodsynopsis
public Imagick::deleteImageArtifact(string $artifact): bool
```

Видаляє артефакт, пов'язаний із зображенням. Різниця між властивостями зображення та артефактами зображення полягає в тому, що властивості є загальнодоступними, а артефакти – приватними. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.5.7 або старшим.

### Список параметрів

`artifact`

Назва артефакту видалення

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Дивіться також

-   [Imagick::setImageArtifact()](imagick.setimageartifact.md) \- Встановлює артефакт зображення
-   [Imagick::getImageArtifact()](imagick.getimageartifact.md) \- Повертає артефакт зображення
