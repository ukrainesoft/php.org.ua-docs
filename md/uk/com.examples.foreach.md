---
navigation:
  - com.examples.md: « Приклади
  - com.examples.arrays.md: Масиви та властивості COM у стилі масивів »
  - index.md: PHP Manual
  - com.examples.md: Приклади
title: For Each
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## For Each

Ви можете використовувати конструкцію [foreach](control-structures.foreach.md) для ітерації контенту стандартного COM/OLE IEnumVariant. Іншими словами, це означає, що ви можете використовувати foreach там, де ви використовували `For Each` у коді VB/ASP.

**Приклад #1 For Each в ASP**

<% Set domainObject = GetObject("WinNT://Domain") For Each obj in domainObject Response.Write obj.Name & "  
" Next %>

**Приклад #2 foreach у PHP**

```php
<?php
$domainObject = new COM("WinNT://Domain");
foreach ($domainObject as $obj) {
   echo $obj->Name . "<br />";
}
?>
```
