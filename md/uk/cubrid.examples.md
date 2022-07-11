- [«Зумовлені константи](cubrid.constants.md)
- [Функції CUBRID »](ref.cubrid.md)

- [PHP Manual](index.md)
- [CUBRID](book.cubrid.md)
- Приклади

# Приклади

Простий приклад, де встановлюється з'єднання з CUBRID. В цьому
розділ розповідається про самі базові речі та особливості, на які
слід звернути увагу. Наступний код здійснюватиме з'єднання з
CUBRID, що передбачає, що сервер та брокер CUBRID запущені.

Приклад нижче використовує базу даних demodb, яка створюється
замовчуванням при установці. Переконайтеся, що її створено.

**Приклад #1 Приклад отримання даних**

` <html>   <head>    <meta http-equiv="content-type" content="text/html; charset=euc-kr">    </head>                   php         /**         ** Задаємо інформація для з'єднання. host_ip - це IP адреса,         ** на которому запущений брокер CUBRID (наприклад, localhost). * host_port - відповідно його порт. * Порт задається за замовчуванням при установці. * Подробиці можна дізнатися в"Administrator's Guide." */    $host_ip ="localhost"; $host_port=33000; $db_name=="demodb"; /**          * З'єднуємося з сервером CUBRID. Не виробляємо фактичного з'єднання, а а тільки одержуємо інформацію про нього. Причина, за якою ми не робимо Фактичного з'єднання, тому, щоб транзакції оброблялися більш */         $cubrid_con = @cubrid_connect($host_ip, $host_port, $db_name); if (!$cubrid_con) {             echo "Помилка підключення к базі даних"; exit; }    ?>    <?php        $sql = "select sports,count(players) as players from event group by sports"; /**          * Запитуємо у сервера CUBRID результат SQL-запиту. * Тепер проводимо фактичне з'єднання з сервером CUBRID. */         $result = cubrid_execute($cubrid_con, $sql); if ($result) {             /**              * Отримуємо імена стовпців із результуючого набору. */             $columns = cubrid_column_names($result); /**               * Отримуємо кількість стовпців в результуючому наборі. */             $num_fields = cubrid_num_cols($result); /**               * Виводимо імена стовпців на екран. */             echo("<tr>"); while(list($key, $colname) = each($columns)) {                echo("<td align=center>$colname</td>"); }             echo("</tr>"); /**               * отримуємо результати із результуючого набору. */             while ($row = cubrid_fetch($result)) {         echo("<tr>"); for ($i = 0; $i < $num_fields; $i++) {                    echo("<td align=center>"); echo($row[$i]); echo("</td>"); }                  echo("</tr>"); }        }         /**         * Модуль PHP в CUBRID працює в трьохрівневій архітектурі. Навіть коли           * викликається SELECT для обробки транзакцій, він обробляється як частина         * транзакції. action. Отже, транзакцію треба підтвердити, або відкатити, навіть коли викликається SELECT. */    cubrid_commit($cubrid_con); cubrid_disconnect($cubrid_con); ?>    </body>    </html>`

**Приклад #2 Приклад вставки даних**

` <html>   <head>   <meta http-equiv="content-type" content="text/html; charset=euc- kr">    </head>     <body>                                          php        /**         * host_ip - IP адрес сервера, где установлен брокер CUBRID         * host_port - порт, на котором он слушает         * db_name - имя базы данных CUBRID         */        $host_ip = "localhost"; $host_port=33000; $db_name=="demodb"; $cubrid_con = @cubrid_connect($host_ip, $host_port, $db_name); if (!$cubrid_con) {             echo "Помилка підключення к базі даних"; exit; }    ?>    <?php        $sql = "insert into olympic (host_year,host_nation,host_city,"            . "opening_date,closing_date) values (2008, 'China', 'Beijing',"            . "to_date('08-08-2008 ','mm-dd- yyyy'),to_date('08-24-2008','mm-dd-yyyy')) ;"; $result = cubrid_execute($cubrid_con, $sql); if ($result) {             /**             ** Обробили успішно, можна фіксувати. */             cubrid_commit($cubrid_con); echo("Inserted successfully "); } else {             /**              ** Відбулася помилка, значить виводимо е на екран і . */             echo(cubrid_error_msg()); cubrid_rollback($cubrid_con); }    cubrid_disconnect($cubrid_con); ?>    </body>    </html>`
