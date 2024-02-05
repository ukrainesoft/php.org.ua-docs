---
navigation:
  - function.cubrid-commit.md: « cubrid\_commit
  - function.cubrid-connect.md: cubrid\_connect »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_connect\_with\_url
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_connect\_with\_url

(PECL CUBRID >= 8.3.1)

cubrid\_connect\_with\_url — Створює оточення для з'єднання із сервером CUBRID

### Опис

```methodsynopsis
cubrid_connect_with_url(    string $conn_url,    string $userid = ?,    string $passwd = ?,    bool $new_link = false): resource
```

Функция**cubrid\_connect\_with\_url()** використовується для створення оточення для з'єднання з сервером за допомогою інформації, заданої у вигляді рядка URL. Якщо в CUBRID дозволена функціональність високої доступності, необхідно встановити інформацію для з'єднання з резервним сервером, яка буде використовуватися для з'єднання, якщо з основним щось трапиться. Якщо логін та пароль не задані, то за умовчанням використовуватиметься з'єднання "PUBLIC".

::= CUBRID::<db\_name>:<db\_user>:<db\_password>:\[? \]

\[&\]

::= alhosts=<alternative\_hosts>\[ &rctime=\]

::= login\_timeout=<milli\_sec>

::= query\_timeout=<milli\_sec>

::= disconnect\_on\_query\_timeout=true|false

<alternative\_hosts> ::= <standby\_broker1\_host>: \[,<standby\_broker2\_host>:\]

:= HOSTNAME | IP\_ADDR

:= SECOND

<milli\_sec> := MILLI SECOND

-   host : Ім'я хоста або IP-адреса основного сервера
-   db\_name : ім'я бази даних
-   db\_user : Ім'я користувача
-   db\_password : пароль
-   alhosts : Задає інформацію про брокера резервного сервера, який буде використовуватися у разі недоступності основного. Якщо ви задасте кілька резервних брокерів, спроби з'єднання будуть відбуватися в тому ж порядку, як вони описані в URL.
-   rctime : Інтервал між спробами підключення до активного брокера, у якому відбувся збій. Після виникнення помилки система з'єднається з резервним брокером, вказаним в althosts (failover), відкотить незавершені транзакції, і потім спробує з'єднатися з активним брокером основного вузла через кожні rctime. Значення за промовчанням 600 секунд.
-   login\_timeout : Максимальний час (мілісекунди) очікування на авторизацію. За умовчанням 0, що означає нескінченний час очікування.
-   query\_timeout : Максимальний час (мілісекунди) очікування на виконання запиту. Після вичерпання цього часу на сервер буде надіслано повідомлення про припинення запиту. Повернене значення запиту залежатиме від налаштування disconnect\_on\_query\_timeout; навіть якщо буде надіслано повідомлення про припинення запиту, він може завершитися вдало.
-   disconnect\_on\_query\_timeout : Визначає, чи повертається помилка відразу після перевищення часу очікування запиту. За замовчуванням\*\*`false`\*\*

> **Зауваження** :
> 
> Символи `?` и `:` є спеціальними в URL-з'єднання і не можуть бути використані в паролі. Приклад некоректного пароля, який не можна використовувати в рядку з'єднання, тому що в ньому використовуються символи "`?:`".
> 
> $url = "CUBRID:localhost:33000:tdb:dba:12?:?login\_timeout=100";
> 
> Пароли, содержащие`?` или `:` можуть бути надіслані окремо.
> 
> $url = "CUBRID:localhost:33000:tbd:::?login\_timeout=100";
> 
> $conn = cubrid\_connect\_with\_url($url, "dba", "12?");
> 
> Якщо логін або пароль порожні, необхідно зберігати символи " `:` ":
> 
> $url = "CUBRID:localhost:33000:demodb:::";

### Список параметрів

`conn_url`

Рядок, що містить інформацію для з'єднання.

`userid`

Ім'я користувача.

`passwd`

пароль.

`new_link`

Якщо функція **cubrid\_connect\_with\_url()** була викликана повторно з такими ж аргументами, нове з'єднання не буде створено, замість нього буде повернено ідентифікатор вже підключення. Параметр `new_link` змінює таку поведінку і змушує **cubrid\_connect\_with\_url()** у будь-якому випадку створити нове з'єднання, навіть якщо функція **cubrid\_connect\_with\_url()** раніше була викликана з такими самими аргументами.

### Значення, що повертаються

Ідентифікатор підключення у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**cubrid\_connect\_with\_url()\*\* без завдання властивостей\*\*

```php
<?php
$conn_url = "CUBRID:localhost:33000:demodb:dba::";
$con = cubrid_connect_with_url($conn_url);

if ($con) {
   echo "connected successfully";
   cubrid_execute($con, "create table person(id int,name char(16))");
   $req =cubrid_execute($con, "insert into person values(1,'James')");

   if ($req) {
      cubrid_close_request($req);
      cubrid_commit($con);
   } else {
      cubrid_rollback($con);
   }
   cubrid_disconnect($con);
}
?>
```

**Пример #2 Пример использования**cubrid\_connect\_with\_url()**с заданием свойств**

```php
<?php
$conn_url = "CUBRID:127.0.0.1:33000:demodb:dba::?login_timeout=100";
$con = cubrid_connect_with_url ($conn_url);

if ($con) {
   echo "connected successfully";
   cubrid_execute($con, "create table person(id int,name char(16))");
   $req =cubrid_execute($con, "insert into person values(1,'James')");

   if ($req) {
      cubrid_close_request($req);
      cubrid_commit($con);
   } else {
      cubrid_rollback($con);
   }
   cubrid_disconnect($con);
}
?>
```

### Дивіться також

-   [cubrid\_connect()](function.cubrid-connect.md) \- Відкриває з'єднання з сервером CUBRID
-   [cubrid\_pconnect()](function.cubrid-pconnect.md) \- Відкриває постійне з'єднання із сервером CUBRID
-   [cubrid\_pconnect\_with\_url()](function.cubrid-pconnect-with-url.md) \- Відкриває постійне з'єднання із сервером CUBRID
-   [cubrid\_disconnect()](function.cubrid-disconnect.md) \- Закриває з'єднання з базою даних
-   [cubrid\_close()](function.cubrid-close.md) \- Закриває з'єднання з базою даних
