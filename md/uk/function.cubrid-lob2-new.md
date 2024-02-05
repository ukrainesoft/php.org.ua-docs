---
navigation:
  - function.cubrid-lob2-import.md: « cubrid\_lob2\_import
  - function.cubrid-lob2-read.md: cubrid\_lob2\_read »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_lob2\_new
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_lob2\_new

(PECL CUBRID >= 8.4.1)

cubrid\_lob2\_new — Створює об'єкт LOB

### Опис

```methodsynopsis
cubrid_lob2_new(resource $conn_identifier = ?, string $type = "BLOB"): resource
```

Функция**cubrid\_lob2\_new()** використовується для створення об'єкта LOB (як BLOB, і CLOB). Її слід використовувати перед прив'язкою LOB.

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання. Якщо ідентифікатор з'єднання не вказано, передбачається останнє підключення, відкрите за допомогою [cubrid\_connect()](function.cubrid-connect.md) або [cubrid\_connect\_with\_url()](function.cubrid-connect-with-url.md)

`type`

Значення має дорівнювати "BLOB" або "CLOB", регістр не враховується. За промовчанням використовується значення "BLOB".

### Значення, що повертаються

Ідентифікатор LOB у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [cubrid\_lob2\_close()](function.cubrid-lob2-close.md) \- Закриває об'єкт LOB
