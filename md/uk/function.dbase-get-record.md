Отримує записи з бази даних як з індексованого масиву

-   [« dbasegetrecordwithnames](function.dbase-get-record-with-names.html)
    
-   [dbasenumfields »](function.dbase-numfields.html)
    
-   [PHP Manual](index.html)
    
-   [dBase](ref.dbase.html)
    
-   Отримує записи з бази даних як з індексованого масиву
    

# dbasegetrecord

(PHP 5 < 5.3.0, dbase 5, dbase 7)

dbasegetrecord — Отримує записи з бази даних, як із індексованого масиву

### Опис

```methodsynopsis
dbase_get_record(resource $database, int $number): array
```

Отримує записи з бази даних як з індексованого масиву.

### Список параметрів

`database`

Ресурс бази даних, що повертається функцією [dbaseopen()](function.dbase-open.html) або [dbasecreate()](function.dbase-create.html)

`number`

Індекс запису (Тут відповідає фізичному номеру запису. - прим. пров.) в діапазоні від `1` до `dbase_numrecords($dbase_identifier)`

### Значення, що повертаються

Повертає запис як масиву. Масив буде включати ключ `deleted` який дорівнює 1, якщо запис позначено видалення (дивіться [dbasedeleterecord()](function.dbase-delete-record.html)

Кожне поле перетворюється на відповідний тип PHP, за винятком:

-   Date перетворюється на рядок.
-   DateTime перетворюється на рядок.
-   Цілі, що виходять із діапазону **`PHP_INT_MIN`\*\*\*\*`PHP_INT_MAX`** перетворюються на рядки.
-   До dbase 7.0.0, логічні значення (`L`) перетворюються на `1` або `0`

У разі виникнення помилки, **dbasegetrecord()** повертає **`false`**

### список змін

| Версия      | Описание                                              |
|-------------|-------------------------------------------------------|
| dbase 7.0.0 | Параметр `database` тепер має тип resource, а не int. |

### Дивіться також

-   [dbasegetrecordwithnames()](function.dbase-get-record-with-names.html) - Отримує запис із бази даних у вигляді асоціативного масиву