---
navigation:
  - oldaliases.cubrid.md: « Застарілі псевдоніми та функції CUBRID
  - function.cubrid-new-glo.md: cubridnewglo »
  - index.md: PHP Manual
  - oldaliases.cubrid.md: Застарілі псевдоніми та функції CUBRID
title: cubridloadfromglo
---
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

-   [cubridnewglo()](function.cubrid-new-glo.md) - Створює екземпляр glo
-   [cubridsaveтоglo()](function.cubrid-save-to-glo.md) - Зберігає запитаний файл в екземплярі GLO
-   [cubridsendglo()](function.cubrid-send-glo.md) - Читання даних з glo та виведення їх у стандартний пристрій виведення
