---
navigation:
  - function.cubrid-new-glo.md: « cubrid\_new\_glo
  - function.cubrid-send-glo.md: cubrid\_send\_glo »
  - index.md: PHP Manual
  - oldaliases.cubrid.md: Застарілі псевдоніми та функції CUBRID
title: cubrid\_save\_to\_glo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_save\_to\_glo

(PECL CUBRID >= 8.3.0)

cubrid\_save\_to\_glo — Зберігає запитаний файл у примірнику GLO

### Опис

```methodsynopsis
cubrid_save_to_glo(resource $conn_identifier, string $oid, string $file_name): int
```

Функция**cubrid\_save\_to\_glo()** використовується для збереження запитаного файлу в екземплярі glo.

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

`oid`

Oid екземпляра glo в якому ви хочете зберегти файл.

`file_name`

Ім'я файлу.

### Значення, що повертаються

**`true`** у разі успішного виконання.

\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** cubrid\_save\_to\_glo()\*\*\*\*

```php
<?php
$req = cubrid_execute ($con, "select image from person where id=1");
if ($req) {
   list ($oid) = cubrid_fetch($req);
   cubrid_close_request($req);
   $res = cubrid_save_to_glo ($con, $oid, "input.jpg");
   if ($res) {
      echo "изображение изменено";
   }
}
?>
```

### Примітки

> **Зауваження** :
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **cubrid\_save\_to\_glo()**

> **Зауваження** :
> 
> Функцію видалено в CUBRID 3.1.

### Дивіться також

-   [cubrid\_new\_glo()](function.cubrid-new-glo.md) \- Створює екземпляр glo
-   [cubrid\_load\_from\_glo()](function.cubrid-load-from-glo.md) \- Читає дані з екземпляра GLO та записує їх у файл
-   [cubrid\_send\_glo()](function.cubrid-send-glo.md) \- Читання даних з glo та виведення їх у стандартний пристрій виведення
