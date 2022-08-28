Повертає рядок

-   [« odbc\_fetch\_object](function.odbc-fetch-object.html)
    
-   [odbc\_field\_len »](function.odbc-field-len.html)
    
-   [PHP Manual](index.html)
    
-   [Функции ODBC](ref.uodbc.html)
    
-   Повертає рядок
    

# odbcfetchrow

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcfetchrow — Повертає рядок

### Опис

```methodsynopsis
odbc_fetch_row(resource $statement, ?int $row = null): bool
```

Вибирає рядок із даних, які були повернуті [odbc\_do()](function.odbc-do.html) або [odbc\_exec()](function.odbc-exec.html). Після виклику **odbcfetchrow()** до полів цього рядка можна отримати доступ за допомогою [odbc\_result()](function.odbc-result.html)

### Список параметрів

`statement`

Ідентифікатор результату.

`row`

Якщо параметр `row` не вказано, **odbcfetchrow()** спробує вибрати наступний рядок у результуючому наборі. Виклики **odbcfetchrow()** з параметром `row` і без нього можна змішувати.

Щоб крок за кроком пройти за результатом більше одного разу, можна викликати **odbcfetchrow()** зі значенням параметра `row`, рівним 1, а потім продовжити виконання **odbcfetchrow()** без `row`, щоб переглянути результат. Якщо драйвер не підтримує вибірку рядків за номером, `row` ігнорується.

### Значення, що повертаються

Повертає **`true`**, якщо рядок існує, **`false`** в іншому випадку.

### список змін

| Версия | Описание                            |
|--------|-------------------------------------|
|        | `row` тепер допускає значення null. |