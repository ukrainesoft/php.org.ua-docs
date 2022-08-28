Закриває з'єднання з базою даних InterBase

-   [« ibase\_blob\_open](function.ibase-blob-open.html)
    
-   [ibase\_commit\_ret »](function.ibase-commit-ret.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Firebird/InterBase](ref.ibase.html)
    
-   Закриває з'єднання з базою даних InterBase
    

# ibaseclose

(PHP 5, PHP 7 < 7.4.0)

ibaseclose — Закриває з'єднання з базою даних InterBase

### Опис

```methodsynopsis
ibase_close(resource $connection_id = null): bool
```

Закриває посилання на базу даних InterBase, пов'язану з ідентифікатором з'єднання, отриманим за допомогою [ibase\_connect()](function.ibase-connect.html). Стандартна транзакція для посилання зафіксована, інші транзакції скасовані.

### Список параметрів

`connection_id`

Ідентифікатор посилання InterBase, отриманий за допомогою [ibase\_connect()](function.ibase-connect.html). Якщо не вказано, передбачається останнє відкрите посилання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ibase\_connect()](function.ibase-connect.html) - Відкриває з'єднання з базою даних
-   [ibase\_pconnect()](function.ibase-pconnect.html) - Відкриває постійне з'єднання з базою даних InterBase