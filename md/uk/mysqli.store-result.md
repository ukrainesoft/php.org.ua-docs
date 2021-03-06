- [« mysqli::stmt_init](mysqli.stmt-init.md)
- [mysqli::$thread_id »](mysqli.thread-id.md)

- [PHP Manual](index.md)
- [mysqli](class.mysqli.md)
- передає на клієнта результуючий набір останнього запиту

# mysqli::store_result

# mysqli_store_result

(PHP 5, PHP 7, PHP 8)

mysqli::store_result -- mysqli_store_result -- Передає на клієнта
результуючий набір останнього запиту

### Опис

Об'єктно-орієнтований стиль

public **mysqli::store_result**(int `$mode` = 0):
[mysqli_result](class.mysqli-result.md)\|false

Процедурний стиль

**mysqli_store_result**([mysqli](class.mysqli.md) `$mysql`, int
`$mode` = 0): [mysqli_result](class.mysqli-result.md)\|false

Передає набір останнього запиту на з'єднанні `mysql`.
Подальша робота з цим набором здійснюється функцією
[mysqli_data_seek()](mysqli-result.data-seek.md).

### Список параметрів

`mysql`
Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md),
отриманий за допомогою [mysqli_connect()](function.mysqli-connect.md)
або [mysqli_init()](mysqli.init.md).

`mode`
Опція, що встановлюється. Може мати одне з наступних значень:

| Ім'я Опис                         |
| --------------------------------- |
| **MYSQLI_STORE_RESULT_COPY_DATA** | Копіює результати з внутрішнього буфера mysqlnd в отримані змінні PHP. За умовчанням mysqlnd використовує посилання, запобігаючи копіюванню та дублювання результатів у пам'яті. У деяких випадках, наприклад, якщо результати містять багато невеликих рядів, копіювання може зменшити загальне споживання пам'яті, тому що змінні PHP, що містять результат, можна звільняти раніше (доступно лише при використанні mysqlnd) 

**Valid options**

### Значення, що повертаються

Повертає буферизований об'єкт результату запиту або **`false`**
у разі помилки.

> **Примітка**:
>
> **mysqli_store_result()** повертає **`false`**, якщо запит не
> повертає результуючої таблиці (наприклад, у разі вираження
> INSERT). Також функція поверне **`false`**, якщо дані з
> результуючого набору не вдалося прочитати. Наявність помилки можна
> перевірити функцією [mysqli_error()](mysqli.error.md), яка в цьому
> у разі поверне непустий рядок; [mysqli_errno()](mysqli.errno.md)
> поверне ненульове значення; і
> [mysqli_field_count()](mysqli.field-count.md) також поверне ненульове
> значення. Також можливою причиною повернення **`false`** після
> успішного виклику [mysqli_query()](mysqli.query.md) може бути
> надто великий результуючий набір (бракує пам'яті для його
> Розміщення). Якщо функція
> [mysqli_field_count()](mysqli.field-count.md) повертає ненульове
> значення, значить, запит повернув непустий результуючий набір.

### Приклади

Дивіться [mysqli_multi_query()](mysqli.multi-query.md).

### Примітки

> **Примітка**:
>
> Навіть попри хорошу практику очищати пам'ять, зайняту результатами
> запитів за допомогою функції
> [mysqli_free_result()](mysqli-result.free.md), якщо
> **mysqli_store_result()** передає великий результуючий набір, це
> може стати проблемою.

### Дивіться також

- [mysqli_real_query()](mysqli.real-query.md) - Виконання SQL
запиту
- [mysqli_use_result()](mysqli.use-result.md) - Готує
результуючий набір на сервері для використання
