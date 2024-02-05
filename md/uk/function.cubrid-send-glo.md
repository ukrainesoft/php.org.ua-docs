---
navigation:
  - function.cubrid-save-to-glo.md: « cubrid\_save\_to\_glo
  - book.dbase.md: dBase »
  - index.md: PHP Manual
  - oldaliases.cubrid.md: Застарілі псевдоніми та функції CUBRID
title: cubrid\_send\_glo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_send\_glo

(PECL CUBRID >= 8.3.0)

cubrid\_send\_glo — Читання даних з glo та виведення їх у стандартний пристрій виведення

### Опис

```methodsynopsis
cubrid_send_glo(resource $conn_identifier, string $oid): int
```

Функция**cubrid\_send\_glo()** використовується для читання даних з glo та виведення їх у стандартний пристрій виведення PHP.

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

`oid`

Oid екземпляра glo з якого ви хочете прочитати дані.

### Значення, що повертаються

**`true`** у разі успішного виконання.

\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** cubrid\_send\_glo()\*\*\*\*

```php
<?php
$req = cubrid_execute ($con, "select image from person where id =1");
if ($req) {
  list ($oid) = cubrid_fetch($req);
  cubrid_close_request($req);
  Header ("Content-type: image/jpeg");
  cubrid_send_glo ($con, $oid);
}
?>
```

### Примітки

> **Зауваження** :
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **cubrid\_send\_glo()**

> **Зауваження** :
> 
> Функцію видалено в CUBRID 3.1.

### Дивіться також

-   [cubrid\_new\_glo()](function.cubrid-new-glo.md) \- Створює екземпляр glo
-   [cubrid\_save\_to\_glo()](function.cubrid-save-to-glo.md) \- Зберігає запитаний файл в екземплярі GLO
-   [cubrid\_load\_from\_glo()](function.cubrid-load-from-glo.md) \- Читає дані з екземпляра GLO та записує їх у файл
