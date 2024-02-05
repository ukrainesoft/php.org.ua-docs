---
navigation:
  - function.cubrid-num-rows.md: « cubrid\_num\_rows
  - function.cubrid-pconnect.md: cubrid\_pconnect »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_pconnect\_with\_url
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_pconnect\_with\_url

(PECL CUBRID >= 8.3.1)

cubrid\_pconnect\_with\_url — Відкриває постійне з'єднання із сервером CUBRID

### Опис

```methodsynopsis
cubrid_pconnect_with_url(string $conn_url, string $userid = ?, string $passwd = ?): resource
```

Встановлює постійне з'єднання із сервером CUBRID.

**cubrid\_pconnect\_with\_url()** діє дуже схоже на [cubrid\_connect\_with\_url()](function.cubrid-connect-with-url.md) з двома основними відмінностями:

По-перше, при підключенні функція спочатку спробує знайти (постійне) посилання, яке вже відкрито з тим самим хостом, портом, ім'ям бази даних та ідентифікатором користувача. Якщо з'єднання буде знайдено, замість відкриття нового буде повернуто його ідентифікатор.

По-друге, з'єднання з SQL-сервером не буде закрито після закінчення скрипту. Натомість посилання залишиться відкритим для використання в майбутньому ([cubrid\_close()](function.cubrid-close.md) або [cubrid\_disconnect()](function.cubrid-disconnect.md) не закриє посилання, встановлені **cubrid\_pconnect\_with\_url()**

Тому цей тип посилання називається "постійним".

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

-   host : Ім'я хоста або IP-адреса основної бази даних
-   db\_name : Ім'я бази даних
-   db\_user : Ім'я користувача бази даних
-   db\_password : Пароль користувача бази даних
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
> $conn = cubrid\_pconnect\_with\_url ($url, "dba", "12?");
> 
> Якщо логін або пароль порожні, необхідно зберігати символи " `:` ":
> 
> $url = "CUBRID:localhost:33000:demodb:::";

### Список параметрів

`conn_url`

Рядок, що містить інформацію для з'єднання.

`userid`

Ім'я користувача бази даних.

`passwd`

Пароль користувача.

### Значення, що повертаються

Ідентифікатор з'єднання у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**cubrid\_pconnect\_with\_url()\*\* без завдання властивостей\*\*

```php
<?php
$conn_url = "CUBRID:127.0.0.1:33000:demodb:dba::";
$con = cubrid_pconnect_with_url ($conn_url);

if ($con) {
   echo "соединение успешно выполнено";
   cubrid_execute($con, "create table person(id int,name char(16))");
   $req =cubrid_execute($con, "insert into person values(1,'James')");

   if ($req) {
      cubrid_close_request ($req);
      cubrid_commit ($con);
   } else {
      cubrid_rollback ($con);
   }
   cubrid_disconnect ($con);
}
?>
```

**Пример #2**cubrid\_pconnect\_with\_url()**url with properties example**

```php
<?php
$conn_url = "CUBRID:127.0.0.1:33000:demodb:dba::?althost=10.34.63.132:33088&rctime=100";
$con = cubrid_pconnect_with_url ($conn_url);

if ($con) {
   echo "соединение успешно выполнено";
   $req =cubrid_execute($con, "insert into person values(1,'James')");

   if ($req) {
      cubrid_close_request ($req);
      cubrid_commit ($con);
   } else {
      cubrid_rollback ($con);
   }
   cubrid_disconnect ($con);
}
?>
```

### Дивіться також

-   [cubrid\_connect()](function.cubrid-connect.md) \- Відкриває з'єднання з сервером CUBRID
-   [cubrid\_connect\_with\_url()](function.cubrid-connect-with-url.md) \- Створює оточення для з'єднання із сервером CUBRID
-   [cubrid\_pconnect()](function.cubrid-pconnect.md) \- Відкриває постійне з'єднання із сервером CUBRID
-   [cubrid\_disconnect()](function.cubrid-disconnect.md) \- Закриває з'єднання з базою даних
-   [cubrid\_close()](function.cubrid-close.md) \- Закриває з'єднання з базою даних
