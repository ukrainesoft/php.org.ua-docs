- [« Imagick::queryFonts](imagick.queryfonts.md)
- [Imagick::radialBlurImage »](imagick.radialblurimage.md)

- [PHP Manual](index.md)
- [Imagick](class.imagick.md)
- Повертає формати, що підтримуються Imagick

# Imagick::queryFormats

(PECL imagick 2, PECL imagick 3)

Imagick::queryFormats — Повертає формати, які підтримує Imagick

### Опис

public static **Imagick::queryFormats**(string `$pattern` = "\*"): array

Повертає формати Imagick.

### Список параметрів

`pattern`

### Значення, що повертаються

Повертає масив, що містить формати, що підтримуються Imagick.

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::queryFormats()****

` <?php    function render() {        $output = ""; $input==Imagick::queryformats(); $ columns = = 6; $output.=="<table|border='2'>"; for ($i=0; $i < count($input); $i += $columns) {            $output .= "<tr>"; for ($c=0;$c<$columns;$c++) {                $output .= "<td>"; if (($i + $c) <  count($input)) {                    $output .= $input[$i + $c]; }                  $output .= "</td>"; }             $output .= "</tr>"; }        $output .= "</table>"; return $output; }?> `
