Повертає частину об'єкта LOB

-   [« OCILob::load](ocilob.load.html)
    
-   [OCILob::rewind »](ocilob.rewind.html)
    
-   [PHP Manual](index.html)
    
-   [OCILob](class.ocilob.html)
    
-   Повертає частину об'єкта LOB
    

# OCILob::read

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

OCILob::read — Повертає частину об'єкта LOB

### Опис

```methodsynopsis
public OCILob::read(int $length): string|false
```

Читає та повертає `length` байт даних із поточної позиції об'єкта LOB.

Читання зупиняється, якщо довжина прочитаних даних дорівнює `length` або якщо досягнуто кінця об'єкта. Внутрішній покажчик переміщається стільки байт, скільки прочитано.

### Список параметрів

`length`

Довжина даних, що зчитуються, в байтах. Великі значення округляються до 1 MB.

### Значення, що повертаються

Повертає вміст у вигляді рядка або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Клас **OCI-Lob** перейменований на [OCILob](class.ocilob.html) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCILob::load](ocilob.load.html)
-   [OCILob::write](ocilob.write.html)