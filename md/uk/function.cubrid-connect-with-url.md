---
navigation:
  - function.cubrid-commit.html: « cubridcommit
  - function.cubrid-connect.html: cubridconnect »
  - index.md: PHP Manual
  - ref.cubrid.md: Функции CUBRID
title: cubridconnectwithurl
---
# cubridconnectwithurl

(PECL CUBRID >= 8.3.1)

cubridconnectwithurl — Створює оточення для з'єднання із сервером CUBRID

### Опис

```methodsynopsis
cubrid_connect_with_url(    string $conn_url,    string $userid = ?,    string $passwd = ?,    bool $new_link = false): resource
```

Функція **cubridconnectwithurl()** використовується для створення оточення для з'єднання з сервером за допомогою інформації, заданої у вигляді рядка URL. Якщо в CUBRID дозволена функціональність високої доступності, необхідно встановити інформацію для з'єднання з резервним сервером, яка буде використовуватися для з'єднання, якщо з основним щось трапиться. Якщо логін та пароль не задані, то за умовчанням використовуватиметься з'єднання "PUBLIC".

::= CUBRID:::::

&

::= alhosts= &rctime=

::= logintimeout=

::= querytimeout=

::= disconnectвінquerytimeout=true|false

::= : ,:

:= HOSTNAME | IPADDR

:= SECOND

:= MILLI SECOND

-   host : Ім'я хоста або IP-адреса основного сервера
-   дбname : ім'я бази даних
-   дбuser : Ім'я користувача
-   дбpassword : пароль
-   alhosts : Задає інформацію про брокера резервного сервера, який буде використовуватись у разі недоступності основного. Якщо ви задасте кілька резервних брокерів, спроби з'єднання будуть відбуватися в тому ж порядку, як вони описані в URL.
-   rctime : Інтервал між спробами підключення до активного брокера, у якому відбувся збій. Після виникнення помилки, система з'єднається з резервним брокерам, вказаним у althosts (failover), відкотить незавершені транзакції, і потім спробує з'єднатися з активним брокером основного вузла через кожні rctime. Значення за промовчанням 600 секунд.
-   logintimeout : Максимальний час (мілісекунди) очікування на авторизацію. За умовчанням 0, що означає нескінченний час очікування.
-   querytimeout : Максимальний час (мілісекунди) очікування на виконання запиту. Після вичерпання цього часу на сервер буде надіслано повідомлення про припинення запиту. Повернене значення запиту залежатиме від налаштування disconnectвінquerytimeout; навіть якщо буде надіслано повідомлення про припинення запиту, він може завершитися вдало.
-   disconnectвінquerytimeout : Визначає, чи повертається помилка відразу після перевищення часу очікування запиту. За замовчуванням **`false`**

> **Зауваження**
> 
> Символи `?` і `:` є спеціальними в URL-з'єднання і не можуть бути використані в паролі. Приклад некоректного пароля, який не можна використовувати в рядку з'єднання, тому що в ньому використовуються символи "`?:`".
> 
> $url = "CUBRID:localhost:33000:tdb:dba:12?:?logintimeout=100";
> 
> Паролі, що містять `?` або `:` можуть бути надіслані окремо.
> 
> $url = "CUBRID:localhost:33000:tbd:::?logintimeout=100";
> 
> $conn = cubridconnectwithurl($url, "dba", "12?");
> 
> Якщо логін або пароль порожні, необхідно зберігати символи "`:`":
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

Якщо функція **cubridconnectwithurl()** була викликана повторно з такими ж аргументами, нове з'єднання не буде створено, замість нього буде повернено ідентифікатор вже підключення. Параметр `new_link` змінює таку поведінку і змушує **cubridconnectwithurl()** у будь-якому випадку створити нове з'єднання, навіть якщо функція **cubridconnectwithurl()** раніше була викликана з такими самими аргументами.

### Значення, що повертаються

Ідентифікатор підключення у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridconnectwithurl()** без завдання властивостей**

```php
<?php
$conn_url = "CUBRID:localhost:33000:demodb:dba::";
$con = cubrid_connect_with_url($conn_url);

if ($con) {
   echo "connected successfully";
   cubrid_execute($con, "create table person(id int,name char(16))");
   $req =cubrid_execute($con, "insert into person values(1,'James')");

   if ($req) {
      cubrid_close_request($req);
      cubrid_commit($con);
   } else {
      cubrid_rollback($con);
   }
   cubrid_disconnect($con);
}
?>
```

**Приклад #2 Приклад використання **cubridconnectwithurl()** із завданням властивостей**

```php
<?php
$conn_url = "CUBRID:127.0.0.1:33000:demodb:dba::?login_timeout=100";
$con = cubrid_connect_with_url ($conn_url);

if ($con) {
   echo "connected successfully";
   cubrid_execute($con, "create table person(id int,name char(16))");
   $req =cubrid_execute($con, "insert into person values(1,'James')");

   if ($req) {
      cubrid_close_request($req);
      cubrid_commit($con);
   } else {
      cubrid_rollback($con);
   }
   cubrid_disconnect($con);
}
?>
```

### Дивіться також

-   [cubridconnect()](function.cubrid-connect.html) - Відкриває з'єднання з сервером CUBRID
-   [cubridpconnect()](function.cubrid-pconnect.html) - Відкриває постійне з'єднання із сервером CUBRID
-   [cubridpconnectwithurl()](function.cubrid-pconnect-with-url.html) - Відкриває постійне з'єднання із сервером CUBRID
-   [cubriddisconnect()](function.cubrid-disconnect.html) - Закриває з'єднання з базою даних
-   [cubridclose()](function.cubrid-close.html) - Закриває з'єднання з базою даних
