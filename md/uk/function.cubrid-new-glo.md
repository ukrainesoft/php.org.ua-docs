---
navigation:
  - function.cubrid-load-from-glo.md: « cubrid\_load\_from\_glo
  - function.cubrid-save-to-glo.md: cubrid\_save\_to\_glo »
  - index.md: PHP Manual
  - oldaliases.cubrid.md: Застарілі псевдоніми та функції CUBRID
title: cubrid\_new\_glo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_new\_glo

(PECL CUBRID >= 8.3.0)

cubrid\_new\_glo — Створює екземпляр glo

### Опис

```methodsynopsis
cubrid_new_glo(resource $conn_identifier, string $class_name, string $file_name): string
```

Функция**cubrid\_new\_glo()** використовується для створення екземпляра glo у запрошеному класі (glo клас). Glo створюється типу LO, і зберігається у файлі `file_name`

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

`class_name`

Назва класу, в якому ви збираєтеся створити glo.

`file_name`

Ім'я файлу.

### Значення, що повертаються

Oid створеного екземпляра у разі успішного виконання.

\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**cubrid\_new\_glo()\*\*\*\*

```php
<?php
$oid = cubrid_new_glo ($con, "glo", "input.jpg");
if ($oid){
   // тип "image" – "object"
   $req = cubrid_execute ($con, "insert into person(image) values($oid)");
   if ($req) {
      echo "картинка была обновлена";
      cubrid_close_request ($req);
      cubrid_commit($con);
   }
}
?>
```

### Примітки

> **Зауваження** :
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **cubrid\_new\_glo()**

> **Зауваження** :
> 
> Функцію видалено в CUBRID 3.1.

### Дивіться також

-   [cubrid\_save\_to\_glo()](function.cubrid-save-to-glo.md) \- Зберігає запитаний файл в екземплярі GLO
-   [cubrid\_load\_from\_glo()](function.cubrid-load-from-glo.md) \- Читає дані з екземпляра GLO та записує їх у файл
-   [cubrid\_send\_glo()](function.cubrid-send-glo.md) \- Читання даних з glo та виведення їх у стандартний пристрій виведення
