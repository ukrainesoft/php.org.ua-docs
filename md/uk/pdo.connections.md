- [«Зумовлені константи](pdo.constants.md)
- [Транзакції та автоматична фіксація змін »](pdo.transactions.md)

- [PHP Manual](index.md)
- [PDO](book.pdo.md)
- Підключення та керування підключеннями

# Підключення та керування підключеннями

З'єднання встановлюються автоматично під час створення об'єкта PDO від нього
базового класу. Не має значення, який драйвер ви хочете
використовувати; Ви завжди використовуєте ім'я базового класу. Конструктор
класу приймає аргументи для завдання джерела даних (DSN), а також
необов'язкові ім'я користувача та пароль (якщо є).

**Приклад #1 Підключення до MySQL**

` <?php$dbh = new PDO('mysql:host=localhost;dbname=test', $user, $pass);?> `

У разі виникнення помилки при підключенні буде викинуто виняток
`PDOException`. Його можна перехопити та обробити, або залишити на
відкуп глобальному обробнику помилок, який ви поставили функцією
[set_exception_handler()](function.set-exception-handler.md).

**Приклад #2 Обробка помилок підключення**

`<?phptry {    $dbh = new PDO('mysql:host=localhost;dbname=test', $user, $pass); foreach($dbh->query('SELECT * from FOO') as $row) {       print_r($row); }   $dbh = null;} catch (PDOException $e) {    print "Error!: " . $e->getMessage() . "<br/>"; die();}?> `

**Увага**

Якщо ваша програма не перехоплює виняток PDO конструктора,
двигун zend виконає стандартні операції для завершення роботи скрипта.
та виведення зворотного трасування. У цьому трасуванні утримуватиметься
детальна інформація про з'єднання з базою даних, включаючи ім'я
користувача та пароль. Відповідальність за перехоплення винятків лежить на
вас. Перехопити виняток можна явно (за допомогою виразу `catch`),
або неявно, поставивши глобальний обробник помилок функцією
[set_exception_handler()](function.set-exception-handler.md).

При успішному підключенні до бази даних у скрипт буде повернено
створений об'єкт PDO. З'єднання залишається активним протягом усього
часу життя. Щоб закрити з'єднання, необхідно знищити
об'єкт шляхом видалення всіх посилань на нього (цього можна домогтися,
привласнюючи **`null`** усім змінним, що вказує на об'єкт). Якщо не
зробити це явно, PHP автоматично закриє з'єднання після закінчення
роботи скрипта.

> **Примітка**: Якщо існують інші посилання на цей екземпляр PDO
> (наприклад, з об'єкта PDOStatement або інші змінні, що посилаються
> на нього), вони також повинні бути видалені (наприклад, присвоєнням
> **`null`** змінної, посилається на PDOStatement).

**Приклад #3 Закриття з'єднання**

` <?php$dbh = new PDO('mysql:host=localhost;dbname=test', $user, $pass); * FROM foo');// з'єднання більше не потрібно, закриваємо$sth = null;$dbh = null;?> `

У багатьох додатках може бути корисним використання постійних
з'єднань до бази даних. Постійні з'єднання не закриваються при
завершення роботи скрипта, вони кешуються і використовуються повторно, коли
інший скрипт запитує з'єднання з тими самими обліковими даними.
Постійні з'єднання дозволяють уникнути створення нових підключень
щоразу, коли потрібен обмін даними з базою, що в результаті дає
приріст швидкості роботи таких програм.

**Приклад #4 Постійні з'єднання**

` <?php$dbh = new PDO('mysql:host=localhost;dbname=test', $user, $pass, array(    PDO::ATTR_PERSISTENT => true));?> `

Значення параметра **`PDO::ATTR_PERSISTENT`** перетворюється на логічне
значення (bool) (включити/вимкнути постійні підключення), якщо це не
числовий рядок (string), який у цьому випадку дозволяє використовувати
кілька пулів постійних підключень. Це корисно, якщо різні
з'єднання використовують несумісні установки, наприклад, різні значення
**`PDO::MYSQL_ATTR_USE_BUFFERED_QUERY`**.

> **Примітка**:
>
> Щоб використовувати постійні з'єднання, потрібно додати
> константу **`PDO::ATTR_PERSISTENT`** у масив параметрів драйвера,
> який передається конструктору PDO. Якщо просто поставити цей атрибут
> функцією [PDO::setAttribute()](pdo.setattribute.md) вже після
> створення об'єкта, драйвер не використовуватиме постійні з'єднання.

> **Примітка**:
>
> Якщо ви використовуєте PDO ODBC драйвер і ваші бібліотеки ODBC
> підтримують об'єднання підключень до пулу (ODBC Connection Pooling)
> (unixODBC і Windows точно підтримують, але можуть бути інші), то
> рекомендується замість постійних з'єднань користуватися цим пулом.
> Пул підключень ODBC доступний для всіх модулів поточного процесу; якщо PDO
> сам кешує з'єднання, то це з'єднання буде недоступне іншим
> модулям і потрапить у пул. В результаті кожен модуль буде створювати
> додаткові підключення для потреб.
