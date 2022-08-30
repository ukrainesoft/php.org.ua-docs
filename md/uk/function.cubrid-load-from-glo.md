Читає дані з екземпляра GLO та записує їх у файл

-   [« Устаревшие псевдонимы и функции CUBRID](oldaliases.cubrid.html)
    
-   [cubridnewglo »](function.cubrid-new-glo.html)
    
-   [PHP Manual](index.html)
    
-   [Устаревшие псевдонимы и функции CUBRID](oldaliases.cubrid.html)
    
-   Читає дані з екземпляра GLO та записує їх у файл
    

# cubridloadfromglo

(PECL CUBRID >= 8.3.0)

cubridloadfromglo — Читає дані з екземпляра GLO та записує їх у файл

### Опис

```methodsynopsis
cubrid_load_from_glo(resource $conn_identifier, string $oid, string $file_name): int
```

Функція **cubridloadfromglo()** використовується для читання даних з екземпляра GLO та запису їх у заданий файл.

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

`oid`

Oid екземпляра glo з якого ви хочете прочитати дані.

`file_name`

Ім'я файлу.

### Значення, що повертаються

**`true`** у разі успішного виконання.

**`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridloadfromglo()****

```php
<?php
$req = cubrid_execute ($con, "select image from person where id=1");
if ($req) {
   list ($oid) = cubrid_fetch($req);
   cubrid_close_request($req);
   $res = cubrid_load_from_glo ($con, $oid, "output.jpg");
   if ($res) {
      echo "Картинка была изменена";
   }
}
?>
```

### Примітки

> **Зауваження**
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **cubridloadfromglo()**

> **Зауваження**
> 
> Функцію видалено в CUBRID 3.1.

### Дивіться також

-   [cubridnewglo()](function.cubrid-new-glo.html) - Створює екземпляр glo
-   [cubridsaveтоglo()](function.cubrid-save-to-glo.html) - Зберігає запитаний файл в екземплярі GLO
-   [cubridsendglo()](function.cubrid-send-glo.html) - Читання даних з glo та виведення їх у стандартний пристрій виведення