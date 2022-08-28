Видалення записів із бази даних

-   [« dbase\_create](function.dbase-create.html)
    
-   [dbase\_get\_header\_info »](function.dbase-get-header-info.html)
    
-   [PHP Manual](index.html)
    
-   [dBase](ref.dbase.html)
    
-   Видалення записів із бази даних
    

# dbasedeleterecord

(PHP 5 < 5.3.0, dbase 5, dbase 7)

dbasedeleterecord — Видалення записів з бази даних

### Опис

```methodsynopsis
dbase_delete_record(resource $database, int $number): bool
```

Позначає записи для видалення з бази даних.

> **Зауваження**
> 
> Для остаточного видалення записів з бази даних необхідно викликати [dbase\_pack()](function.dbase-pack.html)

### Список параметрів

`database`

Ресурс бази даних, що повертається функцією [dbase\_open()](function.dbase-open.html) або [dbase\_create()](function.dbase-create.html)

`number`

Ціле число, в проміжку від 1 до кількості записів у базі динних (кількість записів повертає функція [dbase\_numrecords()](function.dbase-numrecords.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| dbase 7.0.0 | Параметр `database` тепер має тип resource, а не int. |

### Дивіться також

-   [dbase\_add\_record()](function.dbase-add-record.html) - Додає запис до бази даних
-   [dbase\_replace\_record()](function.dbase-replace-record.html) - Замінює запис у базі даних