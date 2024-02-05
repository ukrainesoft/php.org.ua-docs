---
navigation:
  - mysqli.stmt-init.md: '« mysqli::stmt\_init'
  - mysqli.thread-id.md: 'mysqli::$thread\_id »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::store\_result'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::store\_result

# mysqli\_store\_result

(PHP 5, PHP 7, PHP 8)

mysqli::store\_result -- mysqli\_store\_result — Надсилає на клієнта результуючий набір останнього запиту.

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::store_result(int $mode = 0): mysqli_result|false
```

Процедурний стиль

```methodsynopsis
mysqli_store_result(mysqli $mysql, int $mode = 0): mysqli_result|false
```

Надає результуючий набір останнього запиту на з'єднанні `mysql`. Подальша робота з цим набором здійснюється функцією [mysqli\_data\_seek()](mysqli-result.data-seek.md)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

`mode`

Опція, що встановлюється. Починаючи з PHP 8.1 параметр ні на що не впливає. Може мати одне з наступних значень:

**Допустимі варіанти**

| Имя | Опис |
| --- | --- |
| **`MYSQLI_STORE_RESULT_COPY_DATA`** | Копіює результати з внутрішнього буфера mysqlnd в отримані змінні PHP. За умовчанням mysqlnd використовує посилання, запобігаючи копіюванню та дублювання результатів у пам'яті. У деяких випадках, наприклад, якщо результати містять багато невеликих рядів, копіювання може зменшити загальне споживання пам'яті, оскільки змінні PHP, що містять результат, можна звільняти раніше (доступно лише при використанні mysqlnd) |

### Значення, що повертаються

Повертає буферизований об'єкт результату запиту або \*\*`false`\*\*в случае ошибки.

> **Зауваження** :
> 
> **mysqli\_store\_result()** повертає \*\*`false`\*\*якщо запит не повертає результуючої таблиці (наприклад, у разі вираження INSERT). Також функція поверне \*\*`false`\*\*якщо дані з результуючого набору не вдалося прочитати. Наявність помилки можна перевірити функцією [mysqli\_error()](mysqli.error.md), яка у разі поверне непустий рядок; [mysqli\_errno()](mysqli.errno.md) поверне ненульове значення; і [mysqli\_field\_count()](mysqli.field-count.md) також поверне ненульове значення. Також можливою причиною повернення **`false`** після успішного виклику [mysqli\_query()](mysqli.query.md) може бути занадто великий результуючий набір (бракує пам'яті для його розміщення). Якщо функція [mysqli\_field\_count()](mysqli.field-count.md) повертає ненульове значення, тож запит повернув непустий результуючий набір.

### Помилки

Якщо сповіщення про помилки mysqli включено (**`MYSQLI_REPORT_ERROR`**) та запитана операція не вдалася, видається попередження. Якщо, крім того, встановлено режим **`MYSQLI_REPORT_STRICT`**, натомість буде викинуто виняток [mysqli\_sql\_exception](class.mysqli-sql-exception.md)

### Приклади

Смотрите[mysqli\_multi\_query()](mysqli.multi-query.md)

### Примітки

> **Зауваження** :
> 
> Навіть попри гарну практику очищати пам'ять, зайняту результатами запитів, за допомогою функції [mysqli\_free\_result()](mysqli-result.free.md), якщо **mysqli\_store\_result()** передає великий результуючий набір, може стати проблемою.

### Дивіться також

-   [mysqli\_real\_query()](mysqli.real-query.md) \- Виконання SQL запиту
-   [mysqli\_use\_result()](mysqli.use-result.md) \- Готує результуючий набір на сервері для використання
