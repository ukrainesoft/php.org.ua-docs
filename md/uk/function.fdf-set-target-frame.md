---
navigation:
  - function.fdf-set-submit-form-action.md: « fdf\_set\_submit\_form\_action
  - function.fdf-set-value.md: fdf\_set\_value »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdf\_set\_target\_frame
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fdf\_set\_target\_frame

(PHP 4 >= 4.3.0, PHP 5 < 5.3.0, PECL fdf SVN)

fdf\_set\_target\_frame — Встановлює цільовий кадр для відображення форми.

### Опис

```methodsynopsis
fdf_set_target_frame(resource $fdf_document, string $frame_name): bool
```

Встановлює цільовий кадр для відображення PDF-файлу, визначеного за допомогою **fdf\_save\_file()**

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.md) [fdf\_open()](function.fdf-open.md) або [fdf\_open\_string()](function.fdf-open-string.md)

`frame_name`

Фрейм у вигляді рядка.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   **fdf\_save\_file()**
