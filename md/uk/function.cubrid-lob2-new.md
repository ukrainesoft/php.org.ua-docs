---
navigation:
  - function.cubrid-lob2-import.md: « cubridlob2import
  - function.cubrid-lob2-read.md: cubridlob2read »
  - index.md: PHP Manual
  - ref.cubrid.md: Функции CUBRID
title: cubridlob2new
---
# cubridlob2new

(PECL CUBRID >= 8.4.1)

cubridlob2new — Створює об'єкт LOB

### Опис

```methodsynopsis
cubrid_lob2_new(resource $conn_identifier = ?, string $type = "BLOB"): resource
```

Функція **cubridlob2new()** використовується для створення об'єкта LOB (як BLOB, і CLOB). Її слід використовувати перед прив'язкою до об'єкта LOB.

### Список параметрів

`conn_identifier`

Ідентифікатор підключення. Якщо ідентифікатор з'єднання не вказано, передбачається останнє підключення, відкрите за допомогою [cubridconnect()](function.cubrid-connect.md) або [cubridconnectwithurl()](function.cubrid-connect-with-url.md)

`type`

Значення має дорівнювати "BLOB" або "CLOB", регістр не враховується. За промовчанням використовується значення "BLOB".

### Значення, що повертаються

Ідентифікатор LOB у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [cubridlob2close()](function.cubrid-lob2-close.md) - Закриває об'єкт LOB
