Визволяє ресурси, пов'язані з дескриптором LOB

-   [« OCILob::flush](ocilob.flush.md)
    
-   [OCILob::getBuffering »](ocilob.getbuffering.md)
    
-   [PHP Manual](index.md)
    
-   [OCILob](class.ocilob.md)
    
-   Визволяє ресурси, пов'язані з дескриптором LOB
    

# OCILob::free

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

OCILob::free — Звільняє ресурси, пов'язані з дескриптором LOB

### Опис

```methodsynopsis
public OCILob::free(): bool
```

Звільняє ресурси, пов'язані з дескриптором LOB, спочатку виділені функцією [ocinewdescriptor()](function.oci-new-descriptor.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Клас **OCI-Lob** перейменований на [OCILob](class.ocilob.md) відповідно до стандартів іменування PHP. |