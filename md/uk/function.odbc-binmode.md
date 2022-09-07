---
navigation:
  - function.odbc-autocommit.md: « odbcautocommit
  - function.odbc-close-all.md: odbccloseall »
  - index.md: PHP Manual
  - ref.uodbc.md: Функции ODBC
title: odbcbinmode
---
# odbcbinmode

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcbinmode - Керує обробкою двійкових даних стовпця

### Опис

```methodsynopsis
odbc_binmode(resource $statement, int $mode): bool
```

Керує обробкою двійкових даних стовпця. Типи ODBC SQL, що зачіпаються: `BINARY` `VARBINARY` і `LONGVARBINARY`. За замовчуванням можна встановити режим за допомогою директиви php.ini [uodbc.defaultbinmode](odbc.configuration.md#ini.uodbc.defaultbinmode)

Коли двійкові дані SQL перетворюються на символьні дані C (**`ODBC_BINMODE_CONVERT`**), кожен байт (8 біт) вихідних даних представляється як двох символів ASCII. Ці символи є символьним уявленням числа у форматі ASCII у його шістнадцятковій формі. Наприклад, двійкове число `00000001` перетворюється на `"01"` , а `11111111` - у `"FF"`

Хоча обробка стовпців `BINARY` і `VARBINARY` залежить тільки від binmode, обробка стовпців `LONGVARBINARY` також залежить від тривалоговихіду:

**Обробка LONGVARBINARY**

| binmode | longreadlen | result |
| --- | --- | --- |
| **`ODBC_BINMODE_PASSTHRU`** |  | passthru |
| **`ODBC_BINMODE_RETURN`** |  | passthru |
| **`ODBC_BINMODE_CONVERT`** |  | passthru |
| **`ODBC_BINMODE_PASSTHRU`** | \> | passthru |
| **`ODBC_BINMODE_RETURN`** | \> | повернути як є |
| **`ODBC_BINMODE_CONVERT`** | \> | повернути у вигляді char |

Якщо використовується [odbcfetchinto()](function.odbc-fetch-into.md), passthru означає, що для цих стовпців повертається порожній рядок. Якщо використовується [odbcresult()](function.odbc-result.md), passthru означає, що дані надсилаються клієнту безпосередньо (тобто друкуються).

### Список параметрів

`statement`

Ідентифікатор результату.

Якщо `statement` дорівнює `0`, налаштування використовуються за замовчуванням для нових результатів.

`mode`

Можливі значення для `mode`

-   **`ODBC_BINMODE_PASSTHRU`**: Використовувати режим passthru для двійкових даних
-   **`ODBC_BINMODE_RETURN`**: Повернути як є
-   **`ODBC_BINMODE_CONVERT`**: Перетворити на char і повернути

> **Зауваження**: На обробку двійкових стовпців LONG також впливає функція [odbclongreadlen()](function.odbc-longreadlen.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
