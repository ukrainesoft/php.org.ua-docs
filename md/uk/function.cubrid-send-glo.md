---
navigation:
  - function.cubrid-save-to-glo.md: « cubridsaveтоglo
  - book.dbase.md: dBase »
  - index.md: PHP Manual
  - oldaliases.cubrid.md: Застарілі псевдоніми та функції CUBRID
title: cubridsendglo
---
# cubridsendglo

(PECL CUBRID >= 8.3.0)

cubridsendglo — Читання даних із glo та виведення їх у стандартний пристрій виведення

### Опис

```methodsynopsis
cubrid_send_glo(resource $conn_identifier, string $oid): int
```

Функція **cubridsendglo()** використовується для читання даних з glo та виведення їх у стандартний пристрій виведення PHP.

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

`oid`

Oid екземпляра glo з якого ви хочете прочитати дані.

### Значення, що повертаються

**`true`** у разі успішного виконання.

**`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridsendglo()****

```php
<?php
$req = cubrid_execute ($con, "select image from person where id =1");
if ($req) {
  list ($oid) = cubrid_fetch($req);
  cubrid_close_request($req);
  Header ("Content-type: image/jpeg");
  cubrid_send_glo ($con, $oid);
}
?>
```

### Примітки

> **Зауваження**
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **cubridsendglo()**

> **Зауваження**
> 
> Функцію видалено в CUBRID 3.1.

### Дивіться також

-   [cubridnewglo()](function.cubrid-new-glo.md) - Створює екземпляр glo
-   [cubridsaveтоglo()](function.cubrid-save-to-glo.md) - Зберігає запитаний файл в екземплярі GLO
-   [cubridloadfromglo()](function.cubrid-load-from-glo.md) - Читає дані з екземпляра GLO та записує їх у файл
