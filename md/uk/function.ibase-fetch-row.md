---
navigation:
  - function.ibase-fetch-object.html: « ibasefetchobject
  - function.ibase-field-info.html: ibasefieldinfo »
  - index.html: PHP Manual
  - ref.ibase.html: Функции Firebird/InterBase
title: ibasefetchrow
---
# ibasefetchrow

(PHP 5, PHP 7 < 7.4.0)

ibasefetchrow — Витягує рядок із бази даних InterBase

### Опис

```methodsynopsis
ibase_fetch_row(resource $result_identifier, int $fetch_flag = 0): array
```

**ibasefetchrow()** витягує один рядок даних із цього набору результатів.

Наступні дзвінки **ibasefetchrow()** повернуть наступний рядок у наборі результатів або \*\*`false`\*\*якщо рядків більше немає.

### Список параметрів

`result_identifier`

Ідентифікатор результату InterBase.

`fetch_flag`

`fetch_flag` є комбінацією констант **`IBASE_TEXT`** і **`IBASE_UNIXTIME`** ORed. Передача **`IBASE_TEXT`** змусить функцію повертати вміст BLOB-об'єктів замість ідентифікаторів BLOB-об'єктів. Передача **`IBASE_UNIXTIME`** змусить функцію повертати значення дати/часу як позначки часу Unix, а не як відформатовані рядки.

### Значення, що повертаються

Повертає масив, що відповідає обраному рядку, або \*\*`false`\*\*якщо рядків більше немає. Кожен стовпець результату зберігається у зміщенні масиву, починаючи зі зміщення 0.

### Дивіться також

-   [ibasefetchassoc()](function.ibase-fetch-assoc.html) - Витягує рядок результату із запиту у вигляді асоціативного масиву
-   [ibasefetchobject()](function.ibase-fetch-object.html) - Отримує об'єкт із бази даних InterBase
