Встановлення налаштувань

-   [« mysqli::nextresult](mysqli.next-result.html)
    
-   [mysqli::ping »](mysqli.ping.md)
    
-   [PHP Manual](index.md)
    
-   [mysqli](class.mysqli.md)
    
-   Встановлення налаштувань
    

# mysqli::options

# mysqlioptions

(PHP 5, PHP 7, PHP 8)

mysqli::options -- mysqlioptions — Встановлення установок

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

**mysqlioptions()** потрібно викликати після [mysqliinit()](mysqli.init.md) і перед [mysqlirealconnect()](mysqli.real-connect.html)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.html) або [mysqliinit()](mysqli.init.md)

`option`

Налаштування, яке потрібно встановити. Це може бути одне з наступних значень:

**Допустимі налаштування**

| Имя                                     | Описание                                                                                                                                               |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **`MYSQLI_OPT_CONNECT_TIMEOUT`**        | Час очікування з'єднання в секундах                                                                                                                    |
| **`MYSQLI_OPT_READ_TIMEOUT`**           | Час очікування результату виконання команди за секунди. Доступно з PHP 7.2.0.                                                                          |
| **`MYSQLI_OPT_LOCAL_INFILE`**           | Увімкнення/вимкнення `LOAD LOCAL INFILE`                                                                                                               |
| **`MYSQLI_INIT_COMMAND`**               | Команда, яку потрібно виконати одразу після підключення до сервера MySQL                                                                               |
| **`MYSQLI_SET_CHARSET_NAME`**           | Кодування, яке буде встановлено за умовчанням.                                                                                                         |
| **`MYSQLI_READ_DEFAULT_FILE`**          | Читати налаштування з іменованого файлу замість my.cnf Не підтримується mysqlnd.                                                                       |
| **`MYSQLI_READ_DEFAULT_GROUP`**         | Читати налаштування з іменованої групи у файлі my.cnf або іншому файлі, заданим налаштуванням **`MYSQL_READ_DEFAULT_FILE`**. Не підтримується mysqlnd. |
| **`MYSQLI_SERVER_PUBLIC_KEY`**          | p align="justify"> Файл публічного ключа RSA для авторизації на базі SHA-256.                                                                          |
| **`MYSQLI_OPT_NET_CMD_BUFFER_SIZE`**    | Розмір внутрішнього командного/мережевого буфера. Працює лише з mysqlnd.                                                                               |
| **`MYSQLI_OPT_NET_READ_BUFFER_SIZE`**   | Максимальний розмір блоку читання в байтах під час читання командного пакета MySQL. Працює лише з mysqlnd.                                             |
| **`MYSQLI_OPT_INT_AND_FLOAT_NATIVE`**   | Перетворює стовпці типів integer і float до числа PHP, а не рядків. Працює лише з mysqlnd.                                                             |
| **`MYSQLI_OPT_SSL_VERIFY_SERVER_CERT`** | Перевірити сертифікат сервера чи ні.                                                                                                                   |

`value`

Значення параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

Дивіться [mysqlirealconnect()](mysqli.real-connect.html)

### Примітки

> **Зауваження**
> 
> MySQLnd завжди має на увазі кодування, яке використовує за умовчанням сервер. Це кодування передається під час встановлення з'єднання/авторизації, які використовує mysqlnd.
> 
> За замовчуванням Libmysqlclient використовує кодування, встановлене в my.cnf або спеціальним викликом **mysqlioptions()** до використання [mysqlirealconnect()](mysqli.real-connect.html), але після [mysqliinit()](mysqli.init.md)

### Дивіться також

-   [mysqliinit()](mysqli.init.md) - Ініціалізує MySQLi та повертає об'єкт для використання у функції mysqlirealconnect()
-   [mysqlirealconnect()](mysqli.real-connect.html) - Встановлює з'єднання із сервером mysql