Додає код javascript до документа FDF

-   [« FDF](ref.fdf.html)
    
-   [fdfaddtemplate »](function.fdf-add-template.html)
    
-   [PHP Manual](index.html)
    
-   [FDF](ref.fdf.html)
    
-   Додає код javascript до документа FDF
    

# fdfadddocjavascript

(PHP 4> = 4.3.0, PHP 5 <5.3.0, PECL fdf SVN)

fdfadddocjavascript — Додає код javascript до документа FDF

### Опис

```methodsynopsis
fdf_add_doc_javascript(resource $fdf_document, string $script_name, string $script_code): bool
```

Додає скрипт до FDF, який Acrobat потім додає до скрипта документа на рівні документа після того, як у нього буде імпортований FDF.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdfcreate()](function.fdf-create.html) [fdfopen()](function.fdf-open.html) або [fdfopenstring()](function.fdf-open-string.html)

`script_name`

Ім'я сценарію.

`script_code`

Код сценарію. Настійно рекомендується використовувати `\r` для перенесення рядків у коді скрипта.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Додавання коду JavaScript до FDF**

```php
<?php
$fdf = fdf_create();
fdf_add_doc_javascript($fdf, "PlusOne", "function PlusOne(x)\r{\r  return x+1;\r}\r");
fdf_save($fdf);
?>
```

створить FDF наступним чином:

```
%FDF-1.2
%âãÏÓ
1 0 obj
<<
/FDF << /JavaScript << /Doc [ (PlusOne)(function PlusOne\(x\)\r{\r  return x+1;\r}\r)] >> >>
>>
endobj
trailer
<<
/Root 1 0 R

>>
%%EOF
```