Зберігає запитаний файл в екземплярі GLO

-   [« cubridnewglo](function.cubrid-new-glo.html)
    
-   [cubridsendglo »](function.cubrid-send-glo.html)
    
-   [PHP Manual](index.md)
    
-   [Застарілі псевдоніми та функції CUBRID](oldaliases.cubrid.md)
    
-   Зберігає запитаний файл в екземплярі GLO
    

# cubridsaveтоglo

(PECL CUBRID >= 8.3.0)

cubridsaveтоglo — Зберігає запитаний файл у примірнику GLO

### Опис

```methodsynopsis
cubrid_save_to_glo(resource $conn_identifier, string $oid, string $file_name): int
```

Функція **cubridsaveтоglo()** використовується для збереження запитаного файлу в екземплярі glo.

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

`oid`

Oid екземпляра glo в якому ви хочете зберегти файл.

`file_name`

Ім'я файлу.

### Значення, що повертаються

**`true`** у разі успішного виконання.

**`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridsaveтоglo()****

```php
<?php
$req = cubrid_execute ($con, "select image from person where id=1");
if ($req) {
   list ($oid) = cubrid_fetch($req);
   cubrid_close_request($req);
   $res = cubrid_save_to_glo ($con, $oid, "input.jpg");
   if ($res) {
      echo "изображение изменено";
   }
}
?>
```

### Примітки

> **Зауваження**
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **cubridsaveтоglo()**

> **Зауваження**
> 
> Функцію видалено в CUBRID 3.1.

### Дивіться також

-   [cubridnewglo()](function.cubrid-new-glo.html) - Створює екземпляр glo
-   [cubridloadfromglo()](function.cubrid-load-from-glo.html) - Читає дані з екземпляра GLO та записує їх у файл
-   [cubridsendglo()](function.cubrid-send-glo.html) - Читання даних з glo та виведення їх у стандартний пристрій виведення