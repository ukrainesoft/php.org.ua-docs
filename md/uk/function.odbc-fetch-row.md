---
navigation:
  - function.odbc-fetch-object.md: « odbc\_fetch\_object
  - function.odbc-field-len.md: odbc\_field\_len »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_fetch\_row
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_fetch\_row

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_fetch\_row — Повертає рядок

### Опис

```methodsynopsis
odbc_fetch_row(resource $statement, ?int $row = null): bool
```

Вибирає рядок із даних, які були повернуті [odbc\_do()](function.odbc-do.md) або [odbc\_exec()](function.odbc-exec.md). Після виклику **odbc\_fetch\_row()** до полів цього рядка можна отримати доступ за допомогою [odbc\_result()](function.odbc-result.md)

### Список параметрів

`statement`

Ідентифікатор результату.

`row`

Якщо параметр `row` не вказано, **odbc\_fetch\_row()** спробує вибрати наступний рядок у результуючому наборі. Виклики \*\*odbc\_fetch\_row()\*\*с параметром`row` і без нього можна змішувати.

Щоб крок за кроком пройти за результатом більше одного разу, можна викликати \*\*odbc\_fetch\_row()\*\*со значением параметра`row`, рівним 1, а потім продовжити виконання \*\*odbc\_fetch\_row()\*\*без`row`, щоб переглянути результат. Якщо драйвер не підтримує вибірку рядків за номером, `row` ігнорується.

### Значення, що повертаються

Повертає **`true`**, якщо рядок існує, **`false`** в іншому випадку.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `row` тепер допускає значення null. |
