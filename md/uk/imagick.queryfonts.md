---
navigation:
  - imagick.queryfontmetrics.md: '« Imagick::queryFontMetrics'
  - imagick.queryformats.md: 'Imagick::queryFormats »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::queryFonts'
---
# Imagick::queryFonts

(PECL imagick 2, PECL imagick 3)

Imagick::queryFonts — Повертає налаштовані шрифти

### Опис

```methodsynopsis
public static Imagick::queryFonts(string $pattern = "*"): array
```

Повертає налаштовані шрифти.

### Список параметрів

`pattern`

Шаблон запиту

### Значення, що повертаються

Повертає масив, що містить налаштовані шрифти.

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::queryFonts()****

```php
<?php
        $output = '';
        $output .= "Шрифты, соответствующие 'Helvetica*':<br/>";

        $fontList = \Imagick::queryFonts("Helvetica*");

        foreach ($fontList as $fontName) {
            $output .= '<li>'. $fontName."</li>";
        }

        return $output;

?>
```
