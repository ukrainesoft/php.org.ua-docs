Обрізає великий об'єкт

-   [« OCILob::tell](ocilob.tell.html)
    
-   [OCILob::write »](ocilob.write.html)
    
-   [PHP Manual](index.html)
    
-   [OCILob](class.ocilob.html)
    
-   Обрізає великий об'єкт
    

# OCILob::truncate

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

OCILob::truncate — Обрізає великий об'єкт

### Опис

```methodsynopsis
public OCILob::truncate(int $length = 0): bool
```

Обрізає об'єкт LOB.

### Список параметрів

`length`

Якщо вказано, то LOB обрізається до вказаної в `length` довжини у байтах. Інакше LOB повністю очищається.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия                 | Описание                                                                                                |
|------------------------|---------------------------------------------------------------------------------------------------------|
| 8.0.0, PECL OCI8 3.0.0 | Клас **OCI-Lob** перейменований на [OCILob](class.ocilob.html) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCILob::erase](ocilob.erase.html)