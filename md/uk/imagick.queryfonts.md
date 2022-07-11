- [« Imagick::queryFontMetrics](imagick.queryfontmetrics.md)
- [Imagick::queryFormats »](imagick.queryformats.md)

- [PHP Manual](index.md)
- [Imagick](class.imagick.md)
- Повертає налаштовані шрифти

# Imagick::queryFonts

(PECL imagick 2, PECL imagick 3)

Imagick::queryFonts — Повертає налаштовані шрифти

### Опис

public static **Imagick::queryFonts**(string `$pattern` = "\*"): array

Повертає налаштовані шрифти.

### Список параметрів

`pattern`
Шаблон запиту

### Значення, що повертаються

Повертає масив, який містить налаштовані шрифти.

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::queryFonts()****

`<?php        $output = ''; $output .= "Шрифти, відповідні 'Helvetica*':<br/>"; $fontList = \Imagick::queryFonts("Helvetica*"); foreach ($fontList as $fontName) {            $output .= '<li>'. $fontName."</li>"; }    return $output;?> `
