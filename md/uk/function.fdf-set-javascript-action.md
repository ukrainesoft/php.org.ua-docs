Встановлює дію JavaScript для поля

-   [« fdf\_set\_flags](function.fdf-set-flags.html)
    
-   [fdf\_set\_on\_import\_javascript »](function.fdf-set-on-import-javascript.html)
    
-   [PHP Manual](index.html)
    
-   [FDF](ref.fdf.html)
    
-   Встановлює дію JavaScript для поля
    

# fdfsetjavascriptaction

(PHP 4> = 4.0.2, PHP 5 <5.3.0, PECL fdf SVN)

fdfsetjavascriptaction — Встановлює дію javascript для поля

### Опис

```methodsynopsis
fdf_set_javascript_action(    resource $fdf_document,    string $fieldname,    int $trigger,    string $script): bool
```

Встановлює дію JavaScript для заданого поля

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.html) [fdf\_open()](function.fdf-open.html) ор [fdf\_open\_string()](function.fdf-open-string.html)

`fieldname`

Ім'я поля FDF у вигляді рядка.

`trigger`

`script`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fdf\_set\_submit\_form\_action()](function.fdf-set-submit-form-action.html) - Встановлює дію форми надсилання поля