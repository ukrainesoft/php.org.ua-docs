- [«db2_num_fields](function.db2-num-fields.md)
- [db2_pclose »](function.db2-pclose.md)

- [PHP Manual](index.md)
- [Функції IBM DB2](ref.ibm-db2.md)
- Повертає кількість рядків, порушених SQL-запитом

#db2_num_rows

(PECL ibm_db2 \>= 1.0.0)

db2_num_rows — Повертає кількість рядків, порушених SQL-запитом

### Опис

**db2_num_rows**(resource `$stmt`): int

Повертає кількість рядків, видалених, доданих чи оновлених
SQL-запитом.

Щоб визначити кількість рядків, які будуть повернуті оператором
SELECT, введіть SELECT COUNT(\*) з тими самими параметрами, що й
передбачуваний оператор SELECT та отримайте значення.

Якщо логіка вашої програми перевіряє кількість рядків, що повертаються
оператором SELECT та гілок, якщо кількість рядків дорівнює 0, розгляньте
можливість зміни вашої програми, щоб спробувати повернути першу
рядок однієї з функцій
[db2_fetch_assoc()](function.db2-fetch-assoc.md),
[db2_fetch_both()](function.db2-fetch-both.md),
[db2_fetch_array()](function.db2-fetch-array.md) або
[db2_fetch_row()](function.db2-fetch-row.md) і переходьте, якщо
функція вибірки повертає **`false`**.

> **Примітка**:
>
> Якщо ви виконуєте оператор SELECT за допомогою прокручуваного курсору,
> **db2_num_rows()** повертає кількість рядків, що повертаються
> оператором SELECT. Проте накладні витрати, пов'язані з
> курсорами, що прокручуються, значно погіршують продуктивність
> вашої програми, тому, якщо це єдина причина, з якої
> ви розглядаєте можливість використання курсорів, що прокручуються,
> Ви повинні використовувати курсор "forward-only" або викликати SELECT
> COUNT(\*), або покладатися на логічне значення (bool), яке
> повертає значення функцій вибірки для досягнення еквівалентної
> функціональності із значно більшою продуктивністю.

### Список параметрів

`stmt`
Допустимий ресурс `stmt`, що містить набір результатів.

### Значення, що повертаються

Повертає кількість рядків, порушених останнім SQL-оператором,
виданим вказаним дескриптором оператора.
