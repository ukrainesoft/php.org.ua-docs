---
navigation:
  - function.cubrid-get-client-info.md: « cubrid\_get\_client\_info
  - function.cubrid-get-query-timeout.md: cubrid\_get\_query\_timeout »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_get\_db\_parameter
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_get\_db\_parameter

(PECL CUBRID >= 8.3.0)

cubrid\_get\_db\_parameter — Повертає параметри бази даних CUBRID

### Опис

```methodsynopsis
cubrid_get_db_parameter(resource $conn_identifier): array
```

Функція повертає параметри бази даних CUBRID або **`false`** у разі виникнення помилки. Повертається асоціативний масив із значеннями наступних параметрів:

-   **`PARAM_ISOLATION_LEVEL`**
-   **`PARAM_LOCK_TIMEOUT`**
-   **`PARAM_MAX_STRING_LENGTH`**
-   **`PARAM_AUTO_COMMIT`**

**Параметри бази даних**

| Параметр | Опис |
| --- | --- |
| PARAM\_ISOLATION\_LEVEL | Рівень ізоляції транзакції. |
| LOCK\_TIMEOUT | CUBRID надає функцію часу очікування блокування, яка встановлює час очікування (у секундах) для блокування доти, доки не буде дозволено налаштування блокування транзакції. Значення за промовчанням для lock\_timeout\_in\_secs дорівнює -1, що означає, що клієнт програми чекатиме нескінченно, поки блокування транзакції не буде дозволено. |
| PARAM\_AUTO\_COMMIT | У CUBRID PHP режим автоматичної фіксації вимкнено за умовчанням для керування транзакціями. Його можна встановити за допомогою [cubrid\_set\_autocommit()](function.cubrid-set-autocommit.md) |

У наступній таблиці показані рівні ізоляції від 1 до 6. Вона складається зі схеми (рядка) таблиці та рівня ізоляції:

**Рівні ізоляції, які підтримує CUBRID**

| Имя | Опис |
| --- | --- |
| SERIALIZABLE (6) | На цьому рівні ізоляції проблем, пов'язаних з паралелізмом (наприклад, брудне читання, неповторне читання, фантомне читання тощо) не виникає. |
| REPEATABLE READ CLASS з REPEATABLE READ INSTANCES (5) | Інша транзакція T2 не може оновити схему таблиці A, поки транзакція T1 переглядає таблицю A. Транзакція T1 може відчувати фантомне читання для запису R, яка була вставлена ​​іншою транзакцією T2, коли вона повторно отримує певний запис. |
| REPEATABLE READ CLASS з READ COMMITTED INSTANCES (або CURSOR STABILITY) (4) | Інша транзакція T2 не може оновити схему таблиці A, поки транзакція T1 переглядає таблицю A. Транзакція T1 може відчувати читання R (неповторне читання), яке було оновлено та зафіксовано іншою транзакцією T2, коли вона повторно отримує запис R. |
| REPEATABLE READ CLASS з READ UNCOMMITTED INSTANCES (3) | Рівень ізоляції за промовчанням. Інша транзакція T2 не може оновити схему таблиці A, доки транзакція T1 переглядає таблицю A. У транзакції T1 може відбутися читання R (брудне читання) для запису, який був оновлений, але не зафіксований іншою транзакцією T2. |
| READ COMMITTED CLASS з READ COMMITTED INSTANCES (2) | Транзакція T1 може випробовувати читання A' (неповторюване читання) для таблиці, яка була оновлена ​​та зафіксована іншою транзакцією T2, доки вона переглядає таблицю A кілька разів. Транзакція T1 може відчувати читання R' (неповторюване читання) для запису, яка була оновлена ​​та зафіксована іншою транзакцією T2, доки вона повторно отримує запис R. |
| READ COMMITTED CLASS з READ UNCOMMITTED INSTANCES (1) | Транзакція T1 може відчувати читання A' (неповторюване читання) для таблиці, яка була оновлена ​​та зафіксована іншою транзакцією T2, в той час як вона багаторазово переглядає таблицю A. Транзакція T1 може відчувати читання R' (брудне читання) для запису, яка була але не зафіксована іншою транзакцією T2. |

### Список параметрів

`conn_identifier`

З'єднання CUBRID. Якщо ідентифікатор з'єднання не вказано, передбачається останнє посилання, відкрите [cubrid\_connect()](function.cubrid-connect.md)

### Значення, що повертаються

Асоціативний масив з параметрами бази даних CUBRID у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.4.0 | В результаті змінився LOCK\_TIMEOUT на PARAM\_LOCK\_TIMEOUT та MAX\_STRING\_LENGTH на PARAM\_MAX\_STRING\_LENGTH. |

### Приклади

**Приклад #1 Приклад використання** cubrid\_get\_db\_parameter()\*\*\*\*

```php
<?php
printf("%-30s %s\n", "Версия CUBRID PHP:", cubrid_version());

printf("\n");

$conn = cubrid_connect("localhost", 33088, "demodb");

if (!$conn) {
    die('Connect Error ('. cubrid_error_code() .')' . cubrid_error_msg());
}

$db_params = cubrid_get_db_parameter($conn);

while (list($param_name, $param_value) = each($db_params)) {
    printf("%-30s %s\n", $param_name, $param_value);
}

printf("\n");

$server_info = cubrid_get_server_info($conn);
$client_info = cubrid_get_client_info();

printf("%-30s %s\n", "Информация о сервере:", $server_info);
printf("%-30s %s\n", "Информация о клиенте:", $client_info);

printf("\n");

$charset = cubrid_get_charset($conn);

printf("%-30s %s\n", "Кодировка CUBRID:", $charset);

cubrid_disconnect($conn);

?>
```

Результат виконання наведеного прикладу:

```
Версия CUBRID PHP:            9.1.0.0001

PARAM_ISOLATION_LEVEL          3
LOCK_TIMEOUT                   -1
MAX_STRING_LENGTH              1073741823
PARAM_AUTO_COMMIT              1

Информация о сервере:             9.1.0.0212
Информация о клиенте:             9.1.0

Кодировка CUBRID:                iso8859-1
```

### Дивіться також

-   [cubrid\_set\_db\_parameter()](function.cubrid-set-db-parameter.md) \- Встановлює параметри бази даних CUBRID
-   [cubrid\_get\_autocommit()](function.cubrid-get-autocommit.md) \- Повертає налаштування авто-комміту для з'єднання
