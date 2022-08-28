Надає на клієнта результуючий набір останнього запиту

-   [« mysqli::stmt\_init](mysqli.stmt-init.html)
    
-   [mysqli::$thread\_id »](mysqli.thread-id.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Надає на клієнта результуючий набір останнього запиту
    

# mysqli::storeresult

# mysqlistoreresult

(PHP 5, PHP 7, PHP 8)

mysqli::storeresult -- mysqlistoreresult — Надсилає на клієнта результуючий набір останнього запиту.

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::store_result(int $mode = 0): mysqli_result|false
```

Процедурний стиль

```methodsynopsis
mysqli_store_result(mysqli $mysql, int $mode = 0): mysqli_result|false
```

Надає результуючий набір останнього запиту на з'єднанні `mysql`. Подальша робота з цим набором здійснюється функцією [mysqli\_data\_seek()](mysqli-result.data-seek.html)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqli\_connect()](function.mysqli-connect.html) або [mysqli\_init()](mysqli.init.html)

`mode`

Опція, що встановлюється. Може мати одне з таких значень:

**Valid options**

| Имя | Описание |
| --- | --- |
| **`MYSQLI_STORE_RESULT_COPY_DATA`** | Копіює результати з внутрішнього буфера mysqlnd в отримані змінні PHP. За умовчанням mysqlnd використовує посилання, запобігаючи копіюванню та дублювання результатів у пам'яті. У деяких випадках, наприклад, якщо результати містять багато невеликих рядів, копіювання може зменшити загальне споживання пам'яті, оскільки змінні PHP, що містять результат, можна звільняти раніше (доступно лише при використанні mysqlnd) |

### Значення, що повертаються

Повертає буферизований об'єкт результату запиту або **`false`** у разі помилки.

> **Зауваження**
> 
> **mysqlistoreresult()** повертає **`false`**якщо запит не повертає результуючої таблиці (наприклад, у разі вираження INSERT). Також функція поверне **`false`**якщо дані з результуючого набору не вдалося прочитати. Наявність помилки можна перевірити функцією [mysqli\_error()](mysqli.error.html), яка у разі поверне непустий рядок; [mysqli\_errno()](mysqli.errno.html) поверне ненульове значення; і [mysqli\_field\_count()](mysqli.field-count.html) також поверне ненульове значення. Також можливою причиною повернення **`false`** після успішного виклику [mysqli\_query()](mysqli.query.html) може бути занадто великий результуючий набір (бракує пам'яті для його розміщення). Якщо функція [mysqli\_field\_count()](mysqli.field-count.html) повертає ненульове значення, тож запит повернув непустий результуючий набір.

### Приклади

Дивіться [mysqli\_multi\_query()](mysqli.multi-query.html)

### Примітки

> **Зауваження**
> 
> Навіть попри гарну практику очищати пам'ять, зайняту результатами запитів, за допомогою функції [mysqli\_free\_result()](mysqli-result.free.html), якщо **mysqlistoreresult()** передає великий результуючий набір, може стати проблемою.

### Дивіться також

-   [mysqli\_real\_query()](mysqli.real-query.html) - Виконання SQL запиту
-   [mysqli\_use\_result()](mysqli.use-result.html) - Готує результуючий набір на сервері для використання