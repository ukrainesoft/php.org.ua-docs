---
navigation:
  - function.ibase-modify-user.md: « ibase\_modify\_user
  - function.ibase-num-fields.md: ibase\_num\_fields »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_name\_result
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_name\_result

(PHP 5, PHP 7 < 7.4.0)

ibase\_name\_result — Надає ім'я набору результатів.

### Опис

```methodsynopsis
ibase_name_result(resource $result, string $name): bool
```

Функція надає ім'я набору результатів. Ім'я може бути використане пізніше у запитах UPDATE | DELETE ... WHERE CURRENT OF `name`

### Список параметрів

`result`

Набір результатів InterBase.

`name`

Ім'я призначення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**ibase\_name\_result()\*\*\*\*

```php
<?php
$result = ibase_query("SELECT field1,field2 FROM table FOR UPDATE");
ibase_name_result($result, "my_cursor");

$updateqry = ibase_prepare("UPDATE table SET field2 = ? WHERE CURRENT OF my_cursor");

for ($i = 0; ibase_fetch_row($result); ++$i) {
    ibase_execute($updateqry, $i);
}
?>
```

### Дивіться також

-   [ibase\_prepare()](function.ibase-prepare.md) \- готує запит для подальшого зв'язування псевдозмінних та виконання
-   [ibase\_execute()](function.ibase-execute.md) \- Виконує попередньо підготовлений запит
