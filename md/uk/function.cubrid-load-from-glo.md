---
navigation:
  - oldaliases.cubrid.md: « Застарілі псевдоніми та функції CUBRID
  - function.cubrid-new-glo.md: cubrid\_new\_glo »
  - index.md: PHP Manual
  - oldaliases.cubrid.md: Застарілі псевдоніми та функції CUBRID
title: cubrid\_load\_from\_glo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_load\_from\_glo

(PECL CUBRID >= 8.3.0)

cubrid\_load\_from\_glo — Читає дані з екземпляра GLO та записує їх у файл

### Опис

```methodsynopsis
cubrid_load_from_glo(resource $conn_identifier, string $oid, string $file_name): int
```

Функция**cubrid\_load\_from\_glo()** використовується для читання даних з екземпляра GLO та запису їх у заданий файл.

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

`oid`

Oid екземпляра glo з якого ви хочете прочитати дані.

`file_name`

Ім'я файлу.

### Значення, що повертаються

**`true`** у разі успішного виконання.

\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**cubrid\_load\_from\_glo()\*\*\*\*

```php
<?php
$req = cubrid_execute ($con, "select image from person where id=1");
if ($req) {
   list ($oid) = cubrid_fetch($req);
   cubrid_close_request($req);
   $res = cubrid_load_from_glo ($con, $oid, "output.jpg");
   if ($res) {
      echo "Картинка была изменена";
   }
}
?>
```

### Примітки

> **Зауваження** :
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **cubrid\_load\_from\_glo()**

> **Зауваження** :
> 
> Функцію видалено в CUBRID 3.1.

### Дивіться також

-   [cubrid\_new\_glo()](function.cubrid-new-glo.md) \- Створює екземпляр glo
-   [cubrid\_save\_to\_glo()](function.cubrid-save-to-glo.md) \- Зберігає запитаний файл в екземплярі GLO
-   [cubrid\_send\_glo()](function.cubrid-send-glo.md) \- Читання даних з glo та виведення їх у стандартний пристрій виведення
