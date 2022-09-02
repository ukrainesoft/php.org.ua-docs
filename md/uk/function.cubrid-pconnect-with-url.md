---
navigation:
  - function.cubrid-num-rows.md: « cubridnumrows
  - function.cubrid-pconnect.md: cubridpconnect »
  - index.md: PHP Manual
  - ref.cubrid.md: Функции CUBRID
title: cubridpconnectwithurl
---
# cubridpconnectwithurl

(PECL CUBRID >= 8.3.1)

cubridpconnectwithurl — Відкриває постійне з'єднання із сервером CUBRID

### Опис

```methodsynopsis
cubrid_pconnect_with_url(string $conn_url, string $userid = ?, string $passwd = ?): resource
```

Встановлює постійне з'єднання із сервером CUBRID.

**cubridpconnectwithurl()** діє дуже схоже на [cubridconnectwithurl()](function.cubrid-connect-with-url.md) з двома основними відмінностями:

По-перше, при підключенні функція спочатку спробує знайти (постійне) посилання, яке вже відкрито з тим самим хостом, портом, ім'ям бази даних та ідентифікатором користувача. Якщо з'єднання знайдено, замість відкриття нового буде повернуто його ідентифікатор.

По-друге, з'єднання з SQL-сервером не буде закрито після закінчення скрипту. Натомість посилання залишиться відкритим для використання в майбутньому ([cubridclose()](function.cubrid-close.md) або [cubriddisconnect()](function.cubrid-disconnect.md) не закриє посилання, встановлені **cubridpconnectwithurl()**

Тому цей тип посилання називається "постійним".

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

-   host : Ім'я хоста або IP-адреса основної бази даних
-   дбname : Ім'я бази даних
-   дбuser : Ім'я користувача бази даних
-   дбpassword : Пароль користувача бази даних
-   alhosts : Задає інформацію про брокера резервного сервера, який буде використовуватися у разі недоступності основного. Якщо ви задасте кілька резервних брокерів, спроби з'єднання будуть відбуватися в тому ж порядку, як вони описані в URL.
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
> $conn = cubridpconnectwithurl ($ url, "dba", "12?");
> 
> Якщо логін або пароль порожні, необхідно зберігати символи "`:`":
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

Ідентифікатор з'єднання у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridpconnectwithurl()** без завдання властивостей**

```php
<?php
$conn_url = "CUBRID:127.0.0.1:33000:demodb:dba::";
$con = cubrid_pconnect_with_url ($conn_url);

if ($con) {
   echo "соединение успешно выполнено";
   cubrid_execute($con, "create table person(id int,name char(16))");
   $req =cubrid_execute($con, "insert into person values(1,'James')");

   if ($req) {
      cubrid_close_request ($req);
      cubrid_commit ($con);
   } else {
      cubrid_rollback ($con);
   }
   cubrid_disconnect ($con);
}
?>
```

**Приклад #2 **cubridpconnectwithurl()** url with properties example**

```php
<?php
$conn_url = "CUBRID:127.0.0.1:33000:demodb:dba::?althost=10.34.63.132:33088&rctime=100";
$con = cubrid_pconnect_with_url ($conn_url);

if ($con) {
   echo "соединение успешно выполнено";
   $req =cubrid_execute($con, "insert into person values(1,'James')");

   if ($req) {
      cubrid_close_request ($req);
      cubrid_commit ($con);
   } else {
      cubrid_rollback ($con);
   }
   cubrid_disconnect ($con);
}
?>
```

### Дивіться також

-   [cubridconnect()](function.cubrid-connect.md) - Відкриває з'єднання з сервером CUBRID
-   [cubridconnectwithurl()](function.cubrid-connect-with-url.md) - Створює оточення для з'єднання із сервером CUBRID
-   [cubridpconnect()](function.cubrid-pconnect.md) - Відкриває постійне з'єднання із сервером CUBRID
-   [cubriddisconnect()](function.cubrid-disconnect.md) - Закриває з'єднання з базою даних
-   [cubridclose()](function.cubrid-close.md) - Закриває з'єднання з базою даних
