Керує обробкою двійкових даних стовпця

-   [« odbc\_autocommit](function.odbc-autocommit.html)
    
-   [odbc\_close\_all »](function.odbc-close-all.html)
    
-   [PHP Manual](index.html)
    
-   [Функции ODBC](ref.uodbc.html)
    
-   Керує обробкою двійкових даних стовпця
    

# odbcbinmode

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcbinmode - Керує обробкою двійкових даних стовпця

### Опис

```methodsynopsis
odbc_binmode(resource $statement, int $mode): bool
```

Керує обробкою двійкових даних стовпця. Типи ODBC SQL, що зачіпаються: `BINARY` `VARBINARY` і `LONGVARBINARY`. За замовчуванням можна встановити режим за допомогою директиви php.ini [uodbc.defaultbinmode](odbc.configuration.html#ini.uodbc.defaultbinmode)

Коли двійкові дані SQL перетворюються на символьні дані C (**`ODBC_BINMODE_CONVERT`**), кожен байт (8 біт) вихідних даних представляється як двох символів ASCII. Ці символи є символьним уявленням числа у форматі ASCII у його шістнадцятковій формі. Наприклад, двійкове число `00000001` перетворюється на `"01"` , а `11111111` - у `"FF"`

Хоча обробка стовпців `BINARY` і `VARBINARY` залежить тільки від binmode, обробка стовпців `LONGVARBINARY` також залежить від тривалоговихіду:

**Обробка LONGVARBINARY**

| binmode                     | longreadlen | result                   |
|-----------------------------|-------------|--------------------------|
| **`ODBC_BINMODE_PASSTHRU`** |             | passthru                 |
| **`ODBC_BINMODE_RETURN`**   |             | passthru                 |
| **`ODBC_BINMODE_CONVERT`**  |             | passthru                 |
| **`ODBC_BINMODE_PASSTHRU`** | \>          | passthru                 |
| **`ODBC_BINMODE_RETURN`**   | \>          | повернути як є           |
| **`ODBC_BINMODE_CONVERT`**  | \>          | повернути у вигляді char |

Якщо використовується [odbc\_fetch\_into()](function.odbc-fetch-into.html), passthru означає, що для цих стовпців повертається порожній рядок. Якщо використовується [odbc\_result()](function.odbc-result.html), passthru означає, що дані надсилаються клієнту безпосередньо (тобто друкуються).

### Список параметрів

`statement`

Ідентифікатор результату.

Якщо `statement` дорівнює `0`, налаштування використовуються за замовчуванням для нових результатів.

`mode`

Можливі значення для `mode`

-   **`ODBC_BINMODE_PASSTHRU`**: Використовувати режим passthru для двійкових даних
-   **`ODBC_BINMODE_RETURN`**: Повернути як є
-   **`ODBC_BINMODE_CONVERT`**: Перетворити на char і повернути

> **Зауваження**: На обробку двійкових стовпців LONG також впливає функція [odbc\_longreadlen()](function.odbc-longreadlen.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.