For Each

-   [« Примеры](com.examples.html)
    
-   [Масиви та властивості COM у стилі масивів »](com.examples.arrays.html)
    
-   [PHP Manual](index.html)
    
-   [Примеры](com.examples.html)
    
-   For Each
    

## For Each

Ви можете використовувати конструкцію [foreach](control-structures.foreach.html) для ітерації контенту стандартного COM/OLE IEnumVariant. Іншими словами, це означає, що ви можете використовувати foreach там, де ви використовували `For Each` у коді VB/ASP.

**Приклад #1 For Each в ASP**

<% Set domainObject = GetObject("WinNT://Domain") For Each obj in domainObject Response.Write obj.Name & "  
" Next %>

**Приклад #2 foreach у PHP**

```php
<?php
$domainObject = new COM("WinNT://Domain");
foreach ($domainObject as $obj) {
   echo $obj->Name . "<br />";
}
?>
```