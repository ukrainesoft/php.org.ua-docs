---
navigation:
  - imagick.identifyformat.md: '« Imagick::identifyFormat'
  - imagick.implodeimage.md: 'Imagick::implodeImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::identifyImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::identifyImage

(PECL imagick 2, PECL imagick 3)

Imagick::identifyImage — Визначає зображення та отримує атрибути

### Опис

```methodsynopsis
public Imagick::identifyImage(bool $appendRawOutput = false): array
```

Визначає зображення та повертає його атрибути у вигляді масиву. Атрибути зображення включають ширину, висоту, розмір та інші.

### Список параметрів

`appendRawOutput`

Якщо **`true`**, то масив буде включений необроблений висновок.

### Значення, що повертаються

Повертає масив атрибутів. Атрибути зображення включають ширину, висоту, розмір та інші.

### Помилки

Викликає ImagickException у разі виникнення помилки.

**Приклад #1 Приклад результату**

Array (\[imageName\] => /some/path/image.jpg \[format\] => JPEG (Joint Photographic Experts Group JFIF format) \[geometry\] => Array ( \[width\] => 90 \[height\] => 90 )

```
\[type\] => TrueColor
\[colorSpace\] => RGB
\[resolution\] => Array
    (
        \[x\] => 300
        \[y\] => 300
    )

\[units\] => PixelsPerInch
\[fileSize\] => 1.88672kb
\[compression\] => JPEG
\[signature\] => 9a6dc8f604f97d0d691c0286176ddf992e188f0bebba98494b2146ee2d7118da
```

) .
