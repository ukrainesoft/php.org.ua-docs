Створює об'єкт LOB

-   [« cubrid\_lob2\_import](function.cubrid-lob2-import.html)
    
-   [cubrid\_lob2\_read »](function.cubrid-lob2-read.html)
    
-   [PHP Manual](index.html)
    
-   [Функции CUBRID](ref.cubrid.html)
    
-   Створює об'єкт LOB
    

# cubridlob2new

(PECL CUBRID >= 8.4.1)

cubridlob2new — Створює об'єкт LOB

### Опис

```methodsynopsis
cubrid_lob2_new(resource $conn_identifier = ?, string $type = "BLOB"): resource
```

Функція **cubridlob2new()** використовується для створення об'єкта LOB (як BLOB, і CLOB). Її слід використовувати перед прив'язкою до об'єкта LOB.

### Список параметрів

`conn_identifier`

Ідентифікатор підключення. Якщо ідентифікатор з'єднання не вказано, передбачається останнє підключення, відкрите за допомогою [cubrid\_connect()](function.cubrid-connect.html) або [cubrid\_connect\_with\_url()](function.cubrid-connect-with-url.html)

`type`

Значення має дорівнювати "BLOB" або "CLOB", регістр не враховується. За промовчанням використовується значення "BLOB".

### Значення, що повертаються

Ідентифікатор LOB у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [cubrid\_lob2\_close()](function.cubrid-lob2-close.html) - Закриває об'єкт LOB