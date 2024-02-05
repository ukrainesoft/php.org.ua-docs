---
navigation:
  - function.odbc-autocommit.md: « odbc\_autocommit
  - function.odbc-close-all.md: odbc\_close\_all »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_binmode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_binmode

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_binmode - Керує обробкою двійкових даних стовпця

### Опис

```methodsynopsis
odbc_binmode(resource $statement, int $mode): bool
```

Керує обробкою двійкових даних стовпця. Типи ODBC SQL, що зачіпаються: `BINARY` `VARBINARY`и`LONGVARBINARY`. Режим за промовчанням можна встановити за допомогою директиви php.ini [uodbc.defaultbinmode](odbc.configuration.md#ini.uodbc.defaultbinmode)

Коли двійкові дані SQL перетворюються на символьні дані C (**`ODBC_BINMODE_CONVERT`**), кожен байт (8 біт) вихідних даних представляється як двох символів ASCII. Ці символи є символьним уявленням числа у форматі ASCII у його шістнадцятковій формі. Наприклад, двійкове число `00000001`преобразуется в`"01"`, а`11111111` - у `"FF"`

Хотя обработка столбцов`BINARY`и`VARBINARY` залежить тільки від binmode, обробка стовпців `LONGVARBINARY`также зависит от longreadlen:

**Обробка LONGVARBINARY**

| binmode | longreadlen | result |
| --- | --- | --- |
| **`ODBC_BINMODE_PASSTHRU`** |  | passthru |
| **`ODBC_BINMODE_RETURN`** |  | passthru |
| **`ODBC_BINMODE_CONVERT`** |  | passthru |
| **`ODBC_BINMODE_PASSTHRU`** | \> | passthru |
| **`ODBC_BINMODE_RETURN`** | \> | повернути як є |
| **`ODBC_BINMODE_CONVERT`** | \> | повернути у вигляді char |

Якщо використовується [odbc\_fetch\_into()](function.odbc-fetch-into.md), passthru означає, що для цих стовпців повертається порожній рядок. Якщо використовується [odbc\_result()](function.odbc-result.md), passthru означає, що дані надсилаються клієнту безпосередньо (тобто друкуються).

### Список параметрів

`statement`

Ідентифікатор результату.

Якщо `statement`равен , налаштування використовуються за замовчуванням для нових результатів.

`mode`

Можливі значення для `mode` :

-   **`ODBC_BINMODE_PASSTHRU`**: Використовувати режим passthru для двійкових даних
-   **`ODBC_BINMODE_RETURN`**: Повернути як є
-   **`ODBC_BINMODE_CONVERT`**: Перетворити на char і повернути

> **Зауваження**: На обробку двійкових стовпців LONG також впливає функція [odbc\_longreadlen()](function.odbc-longreadlen.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
