---
navigation:
  - mysqli.next-result.md: '« mysqli::next\_result'
  - mysqli.ping.md: 'mysqli::ping »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::options'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::options

# mysqli\_options

(PHP 5, PHP 7, PHP 8)

mysqli::options -- mysqli\_options — Встановлення установок

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::options(int $option, string|int $value): bool
```

Процедурний стиль

```methodsynopsis
mysqli_options(mysqli $mysql, int $option, string|int $value): bool
```

Використовується для встановлення додаткових параметрів з'єднання та поведінки підключення до бази даних.

Цю функцію можна викликати неодноразово, щоб встановити кілька налаштувань.

**mysqli\_options()** потрібно викликати після [mysqli\_init()](mysqli.init.md)и перед[mysqli\_real\_connect()](mysqli.real-connect.md)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

`option`

Налаштування, яке потрібно встановити. Це може бути одне з наступних значень:

**Допустимі налаштування**

| Имя | Опис |
| --- | --- |
| **`MYSQLI_OPT_CONNECT_TIMEOUT`** | Час очікування з'єднання в секундах |
| **`MYSQLI_OPT_READ_TIMEOUT`** | Час очікування результату виконання команди за секунди. Доступно з PHP 7.2.0. |
| **`MYSQLI_OPT_LOCAL_INFILE`** | Увімкнення/вимкнення `LOAD LOCAL INFILE` |
| **`MYSQLI_INIT_COMMAND`** | Команда, яку потрібно виконати одразу після підключення до сервера MySQL |
| **`MYSQLI_SET_CHARSET_NAME`** | Кодування, яке буде встановлено за умовчанням. |
| **`MYSQLI_READ_DEFAULT_FILE`** | Читати налаштування з іменованого файлу замість my.cnf Не підтримується mysqlnd. |
| **`MYSQLI_READ_DEFAULT_GROUP`** | Читати налаштування з іменованої групи у файлі my.cnf або іншому файлі, заданим налаштуванням **`MYSQL_READ_DEFAULT_FILE`**. . Не підтримується mysqlnd. |
| **`MYSQLI_SERVER_PUBLIC_KEY`** | p align="justify"> Файл публічного ключа RSA для авторизації на базі SHA-256. |
| **`MYSQLI_OPT_NET_CMD_BUFFER_SIZE`** | Розмір внутрішнього командного/мережевого буфера. Працює лише з mysqlnd. |
| **`MYSQLI_OPT_NET_READ_BUFFER_SIZE`** | Максимальний розмір блоку читання в байтах під час читання командного пакета MySQL. Працює лише з mysqlnd. |
| **`MYSQLI_OPT_INT_AND_FLOAT_NATIVE`** | Перетворює стовпці типів integer і float до числа PHP при використанні непідготовлених виразів. Працює лише з mysqlnd. |
| **`MYSQLI_OPT_SSL_VERIFY_SERVER_CERT`** | Перевірити сертифікат сервера чи ні. |

`value`

Значення параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Якщо сповіщення про помилки mysqli включено (**`MYSQLI_REPORT_ERROR`**) та запитана операція не вдалася, видається попередження. Якщо, крім того, встановлено режим **`MYSQLI_REPORT_STRICT`**, натомість буде викинуто виняток [mysqli\_sql\_exception](class.mysqli-sql-exception.md)

### Приклади

Смотрите[mysqli\_real\_connect()](mysqli.real-connect.md)

### Примітки

> **Зауваження** :
> 
> MySQLnd завжди має на увазі кодування, яке використовує за умовчанням сервер. Це кодування передається під час встановлення з'єднання/авторизації, які використовує mysqlnd.
> 
> За замовчуванням Libmysqlclient використовує кодування, встановлене у файлі my.cnf або явним викликом функції **mysqli\_options()** до виклику функції [mysqli\_real\_connect()](mysqli.real-connect.md), але після виклику функції [mysqli\_connect()](function.mysqli-connect.md)

### Дивіться також

-   [mysqli\_init()](mysqli.init.md) \- Ініціалізує MySQLi та повертає об'єкт для використання у функції mysqli\_real\_connect()
-   [mysqli\_real\_connect()](mysqli.real-connect.md) \- Встановлює з'єднання із сервером mysql
