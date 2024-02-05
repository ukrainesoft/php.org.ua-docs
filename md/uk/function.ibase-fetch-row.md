---
navigation:
  - function.ibase-fetch-object.md: « ibase\_fetch\_object
  - function.ibase-field-info.md: ibase\_field\_info »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_fetch\_row
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_fetch\_row

(PHP 5, PHP 7 < 7.4.0)

ibase\_fetch\_row — Витягує рядок із бази даних InterBase

### Опис

```methodsynopsis
ibase_fetch_row(resource $result_identifier, int $fetch_flag = 0): array
```

**ibase\_fetch\_row()** витягує один рядок даних із цього набору результатів.

Наступні дзвінки \*\*ibase\_fetch\_row()**вернут следующую строку в наборе результатов или**`false`\*\*якщо рядків більше немає.

### Список параметрів

`result_identifier`

Ідентифікатор результату InterBase.

`fetch_flag`

`fetch_flag` є комбінацією констант **`IBASE_TEXT`** і **`IBASE_UNIXTIME`**ORed. Передача**`IBASE_TEXT`** змусить функцію повертати вміст BLOB-об'єктів замість ідентифікаторів BLOB-об'єктів. Передача **`IBASE_UNIXTIME`** змусить функцію повертати значення дати/часу як позначки часу Unix, а не як відформатовані рядки.

### Значення, що повертаються

Повертає масив, що відповідає обраному рядку, або \*\*`false`\*\*якщо рядків більше немає. Кожен стовпець результату зберігається у зміщенні масиву, починаючи зі зміщення 0.

### Дивіться також

-   [ibase\_fetch\_assoc()](function.ibase-fetch-assoc.md) \- Витягує рядок результату із запиту у вигляді асоціативного масиву
-   [ibase\_fetch\_object()](function.ibase-fetch-object.md) \- Отримує об'єкт із бази даних InterBase
