---
navigation:
  - function.ibase-execute.md: « ibase\_execute
  - function.ibase-fetch-object.md: ibase\_fetch\_object »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_fetch\_assoc
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_fetch\_assoc

(PHP 5, PHP 7 < 7.4.0)

ibase\_fetch\_assoc — Витягує рядок результату із запиту у вигляді асоціативного масиву

### Опис

```methodsynopsis
ibase_fetch_assoc(resource $result, int $fetch_flag = 0): array
```

Витягує рядок результату із запиту у вигляді асоціативного масиву

**ibase\_fetch\_assoc()** витягує один рядок даних із результату. Якщо два або більше стовпця результату мають однакові назви полів, останній стовпець матиме пріоритет. Щоб отримати доступ до інших стовпців з тим же ім'ям, вам потрібно отримати доступ до результату за допомогою числових індексів функцією [ibase\_fetch\_row()](function.ibase-fetch-row.md)або використовувати псевдоніми у своєму запиті.

### Список параметрів

`result`

Дескриптор результату.

`fetch_flag`

`fetch_flag` є комбінацією констант **`IBASE_TEXT`**и**`IBASE_UNIXTIME`**ORed. Передача**`IBASE_TEXT`** змусить функцію повертати вміст BLOB-об'єктів замість ідентифікаторів BLOB-об'єктів. Передача **`IBASE_UNIXTIME`** змусить функцію повертати значення дати/часу як позначки часу Unix, а не як відформатовані рядки.

### Значення, що повертаються

Повертає асоціативний масив, що відповідає обраному рядку. Наступні дзвінки повернуть наступний рядок у наборі результатів або \*\*`false`\*\*якщо рядків більше немає.

### Дивіться також

-   [ibase\_fetch\_row()](function.ibase-fetch-row.md) \- Витягує рядок із бази даних InterBase
-   [ibase\_fetch\_object()](function.ibase-fetch-object.md) \- Отримує об'єкт із бази даних InterBase
