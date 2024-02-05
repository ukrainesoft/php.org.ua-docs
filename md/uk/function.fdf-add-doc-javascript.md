---
navigation:
  - ref.fdf.md: « FDF
  - function.fdf-add-template.md: fdf\_add\_template »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdf\_add\_doc\_javascript
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fdf\_add\_doc\_javascript

(PHP 4 >= 4.3.0, PHP 5 < 5.3.0, PECL fdf SVN)

fdf\_add\_doc\_javascript — Додає код javascript до документа FDF

### Опис

```methodsynopsis
fdf_add_doc_javascript(resource $fdf_document, string $script_name, string $script_code): bool
```

Додає скрипт до FDF, який Acrobat потім додає до скрипта документа на рівні документа після того, як у нього буде імпортований FDF.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.md) [fdf\_open()](function.fdf-open.md) або [fdf\_open\_string()](function.fdf-open-string.md)

`script_name`

Ім'я сценарію.

`script_code`

Код сценарію. Настійно рекомендується використовувати `\r`для переноса строк в коде скрипта.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Додавання коду JavaScript до FDF**

```php
<?php
$fdf = fdf_create();
fdf_add_doc_javascript($fdf, "PlusOne", "function PlusOne(x)\r{\r  return x+1;\r}\r");
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
