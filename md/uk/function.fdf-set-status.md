Встановлює значення ключа /STATUS

-   [« fdfsetopt](function.fdf-set-opt.html)
    
-   [fdfsetsubmitformaction »](function.fdf-set-submit-form-action.html)
    
-   [PHP Manual](index.html)
    
-   [FDF](ref.fdf.html)
    
-   Встановлює значення ключа /STATUS
    

# fdfsetstatus

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdfsetstatus — Встановлює значення ключа /STATUS

### Опис

```methodsynopsis
fdf_set_status(resource $fdf_document, string $status): bool
```

Встановлює значення ключа `/STATUS`. Коли клієнт отримує FDF із встановленим статусом, він представляє значення у вікні попередження.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdfcreate()](function.fdf-create.html) [fdfopen()](function.fdf-open.html) ор [fdfopenstring()](function.fdf-open-string.html)

`status`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fdfgetstatus()](function.fdf-get-status.html) - Отримує значення ключа /STATUS