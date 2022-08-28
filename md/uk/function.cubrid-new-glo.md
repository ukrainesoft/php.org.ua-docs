Створює екземпляр glo

-   [« cubrid\_load\_from\_glo](function.cubrid-load-from-glo.html)
    
-   [cubrid\_save\_to\_glo »](function.cubrid-save-to-glo.html)
    
-   [PHP Manual](index.html)
    
-   [Устаревшие псевдонимы и функции CUBRID](oldaliases.cubrid.html)
    
-   Створює екземпляр glo
    

# cubridnewglo

(PECL CUBRID >= 8.3.0)

cubridnewglo — Створює екземпляр glo

### Опис

```methodsynopsis
cubrid_new_glo(resource $conn_identifier, string $class_name, string $file_name): string
```

Функція **cubridnewglo()** використовується для створення екземпляра glo у запрошеному класі (glo клас). Glo створюється типу LO, і зберігається у файлі `file_name`

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

`class_name`

Назва класу, в якому ви збираєтеся створити glo.

`file_name`

Ім'я файлу.

### Значення, що повертаються

Oid створеного екземпляра у разі успішного виконання.

**`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridnewglo()****

```php
<?php
$oid = cubrid_new_glo ($con, "glo", "input.jpg");
if ($oid){
   // тип "image" – "object"
   $req = cubrid_execute ($con, "insert into person(image) values($oid)");
   if ($req) {
      echo "картинка была обновлена";
      cubrid_close_request ($req);
      cubrid_commit($con);
   }
}
?>
```

### Примітки

> **Зауваження**
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **cubridnewglo()**

> **Зауваження**
> 
> Функцію видалено в CUBRID 3.1.

### Дивіться також

-   [cubrid\_save\_to\_glo()](function.cubrid-save-to-glo.html) - Зберігає запитаний файл в екземплярі GLO
-   [cubrid\_load\_from\_glo()](function.cubrid-load-from-glo.html) - Читає дані з екземпляра GLO та записує їх у файл
-   [cubrid\_send\_glo()](function.cubrid-send-glo.html) - Читання даних з glo та виведення їх у стандартний пристрій виведення