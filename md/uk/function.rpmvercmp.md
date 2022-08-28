Порівняння версій двох RPM

-   [« rpminfo](function.rpminfo.html)
    
-   [XLSWriter »](book.xlswriter.html)
    
-   [PHP Manual](index.html)
    
-   [Функции RpmInfo](ref.rpminfo.html)
    
-   Порівняння версій двох RPM
    

# rpmvercmp

(PECL rpminfo >= 0.1.0)

rpmvercmp - Порівняння версій двох RPM

### Опис

```methodsynopsis
rpmvercmp(string $evr1, string $evr2): int
```

Порівняння двох версій RPM.

### Список параметрів

`evr1`

Перша версія у форматі epoch:version-release

`evr2`

Друга версія у форматі epoch:version-release

### Значення, що повертаються

Повертає < 0, якщо evr1 менше evr2, > 0 якщо evr1 більше evr2 та 0, якщо вони ідентичні.