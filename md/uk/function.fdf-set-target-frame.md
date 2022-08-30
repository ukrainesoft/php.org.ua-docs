Встановлює цільовий кадр для відображення форми

-   [« fdfsetsubmitformaction](function.fdf-set-submit-form-action.html)
    
-   [fdfsetvalue »](function.fdf-set-value.html)
    
-   [PHP Manual](index.html)
    
-   [FDF](ref.fdf.html)
    
-   Встановлює цільовий кадр для відображення форми
    

# fdfsettargetframe

(PHP 4> = 4.3.0, PHP 5 <5.3.0, PECL fdf SVN)

fdfsettargetframe — Встановлює цільовий кадр для відображення форми.

### Опис

```methodsynopsis
fdf_set_target_frame(resource $fdf_document, string $frame_name): bool
```

Встановлює цільовий кадр для відображення PDF-файлу, визначеного за допомогою **fdfsavefile()**

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdfcreate()](function.fdf-create.html) [fdfopen()](function.fdf-open.html) або [fdfopenstring()](function.fdf-open-string.html)

`frame_name`

Фрейм у вигляді рядка.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   **fdfsavefile()**