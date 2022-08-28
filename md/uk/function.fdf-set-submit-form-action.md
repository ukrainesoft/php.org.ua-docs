Встановлює дію форми надсилання поля

-   [« fdf\_set\_status](function.fdf-set-status.html)
    
-   [fdf\_set\_target\_frame »](function.fdf-set-target-frame.html)
    
-   [PHP Manual](index.html)
    
-   [FDF](ref.fdf.html)
    
-   Встановлює дію форми надсилання поля
    

# fdfsetsubmitformaction

(PHP 4> = 4.0.2, PHP 5 <5.3.0, PECL fdf SVN)

fdfsetsubmitformaction — Встановлює дію форми надсилання поля

### Опис

```methodsynopsis
fdf_set_submit_form_action(    resource $fdf_document,    string $fieldname,    int $trigger,    string $script,    int $flags): bool
```

Встановлює дію форми надсилання для заданого поля.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.html) [fdf\_open()](function.fdf-open.html) або [fdf\_open\_string()](function.fdf-open-string.html)

`fieldname`

Ім'я поля FDF у вигляді рядка.

`trigger`

`script`

`flags`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fdf\_set\_javascript\_action()](function.fdf-set-javascript-action.html) - Встановлює дію JavaScript для поля