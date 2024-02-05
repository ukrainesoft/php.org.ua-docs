---
navigation:
  - imagick.queryfonts.md: '« Imagick::queryFonts'
  - imagick.radialblurimage.md: 'Imagick::radialBlurImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::queryFormats'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::queryFormats

(PECL imagick 2, PECL imagick 3)

Imagick::queryFormats — Повертає формати, які підтримує Imagick

### Опис

```methodsynopsis
public static Imagick::queryFormats(string $pattern = "*"): array
```

Повертає формати Imagick.

### Список параметрів

`pattern`

### Значення, що повертаються

Повертає масив, що містить формати, що підтримуються Imagick.

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Пример #1 Пример использования**Imagick::queryFormats()\*\*\*\*

```php
<?php
    function render() {
        $output = "";
        $input = \Imagick::queryformats();
        $columns = 6;

        $output .= "<table border='2'>";

        for ($i=0; $i < count($input); $i += $columns) {
            $output .= "<tr>";
            for ($c=0; $c<$columns; $c++) {
                $output .= "<td>";
                if (($i + $c) <  count($input)) {
                    $output .= $input[$i + $c];
                }
                $output .= "</td>";
            }
            $output .= "</tr>";
        }

        $output .= "</table>";

        return $output;
    }

?>
```
