---
navigation:
  - cubrid.constants.md: « Обумовлені константи
  - ref.cubrid.md: Функции CUBRID »
  - index.md: PHP Manual
  - book.cubrid.md: CUBRID
title: Приклади
---
# Приклади

Простий приклад, у якому встановлюється з'єднання з CUBRID. У цьому розділі розповідається про самі базові речі та особливості, на які слід звернути увагу. Наступний код здійснюватиме з'єднання з CUBRID, що передбачає, що сервер та брокер CUBRID запущені.

Приклад нижче використовує базу даних demodb, яка створюється за умовчанням під час встановлення. Переконайтеся, що її створено.

**Приклад #1 Приклад отримання даних**

```php
<html>
    <head>
    <meta http-equiv="content-type" content="text/html; charset=euc-kr">
    </head>
    <body>
    <center>
    <table border=2>
    <?php
        /**
         * Задаём информация для соединения. host_ip - это IP адрес,
         * на котором запущен брокер CUBRID (например, localhost).
         * host_port - соответственно его порт.
         * Порт задаётся по умолчанию при установке.
         * Подробности можно узнать в "Administrator's Guide."
         */
        $host_ip = "localhost";
        $host_port = 33000;
        $db_name = "demodb";
        /**
         * Соединяемся с сервером CUBRID. Не производим фактического соединения, а
         * только получаем информацию о нем. Причина, по которой мы не делаем
         * фактического соединения в том, чтобы транзакции обрабатывались более
         * эффективно в трёхзвенной архитектуре.
         */
        $cubrid_con = @cubrid_connect($host_ip, $host_port, $db_name);

        if (!$cubrid_con) {
            echo "Ошибка подключения к базе данных";
            exit;
        }
    ?>
    <?php
        $sql = "select sports, count(players) as players from event group by sports";
        /**
         * Запрашиваем у сервера CUBRID результат SQL-запроса.
         * Теперь производим фактическое соединение с сервером CUBRID.
         */
        $result = cubrid_execute($cubrid_con, $sql);

        if ($result) {
            /**
             * Получаем имена столбцов из результирующего набора.
             */
            $columns = cubrid_column_names($result);
            /**
             * Получаем количество столбцов в результирующем наборе.
             */
            $num_fields = cubrid_num_cols($result);
            /**
             * Выводим имена столбцов на экран.
             */
            echo("<tr>");

            while (list($key, $colname) = each($columns)) {
                echo("<td align=center>$colname</td>");
            }

            echo("</tr>");

            /**
             * получаем результаты из результирующего набора.
             */
            while ($row = cubrid_fetch($result)) {
                echo("<tr>");

                for ($i = 0; $i < $num_fields; $i++) {
                    echo("<td align=center>");
                    echo($row[$i]);
                    echo("</td>");
                }

                echo("</tr>");
            }
        }
        /**
         * Модуль PHP в CUBRID работает в трёхуровневой архитектуре. Даже когда
         * вызывается SELECT для обработки транзакций, он обрабатывается как часть
         * транзакции. action. Следовательно, транзакцию надо либо подтвердить, либо
         * откатить, даже когда вызывается SELECT.
         */
        cubrid_commit($cubrid_con);
        cubrid_disconnect($cubrid_con);
    ?>
    </body>
    </html>
```

**Приклад #2 Приклад вставки даних**

```php
<html>
    <head>
    <meta http-equiv="content-type" content="text/html; charset=euc- kr">
    </head>
    <body>
    <center>
    <table border=2>
    <?php
        /**
         * host_ip - IP адрес сервера, где установлен брокер CUBRID
         * host_port - порт, на котором он слушает
         * db_name - имя базы данных CUBRID
         */
        $host_ip = "localhost";
        $host_port = 33000;
        $db_name = "demodb";
        $cubrid_con = @cubrid_connect($host_ip, $host_port, $db_name);

        if (!$cubrid_con) {
            echo "Ошибка подключения к базе данных";
            exit;
        }
    ?>
    <?php
        $sql = "insert into olympic (host_year,host_nation,host_city,"
            . "opening_date,closing_date) values (2008, 'China', 'Beijing',"
            . "to_date('08-08-2008','mm-dd- yyyy'),to_date('08-24-2008','mm-dd-yyyy')) ;";
        $result = cubrid_execute($cubrid_con, $sql);
        if ($result) {
            /**
             * Обработали успешно, можно фиксировать.
             */
            cubrid_commit($cubrid_con);
            echo("Inserted successfully ");
        } else {
            /**
             * Произошла ошибка, значит выводим её на экран и откатываемся.
             */
            echo(cubrid_error_msg());
            cubrid_rollback($cubrid_con);
        }
        cubrid_disconnect($cubrid_con);
    ?>
    </body>
    </html>
```
