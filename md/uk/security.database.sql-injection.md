---
navigation:
  - security.database.storage.md: « Шифрування сховища бази даних
  - security.errors.md: Повідомлення про помилки »
  - index.md: PHP Manual
  - security.database.md: Безпека баз даних
title: SQL-ін'єкції
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## SQL-ін'єкції

SQL-ін'єкція - це техніка, за якої зловмисник використовує недоліки в коді програми, що відповідає за побудову динамічних SQL-запитів. Зловмисник може отримати доступ до привілейованих розділів програми, отримати всю інформацію з бази даних, підмінити наявні дані або навіть виконати небезпечні команди системного рівня на вузлі бази даних. Уразливість виникає, коли розробники конкатенують або інтерполують довільне введення SQL-запитах.

**Приклад #1 Посторінковий висновок результату та створення суперкористувача в PostgreSQL**

У наступному прикладі введення користувача інтерполується в SQL-запит, що дозволяє зловмиснику отримати обліковий запис суперкористувача в базі даних.

```php
<?php

$offset = $_GET['offset']; // осторожно, нет валидации ввода!
$query  = "SELECT id, name FROM products ORDER BY name LIMIT 20 OFFSET $offset;";
$result = pg_query($conn, $query);
?>
```

Зазвичай користувачі натискають за посиланням 'вперед' і 'назад', внаслідок чого значення змінної $offset заноситься до URL. Скрипт очікує, що $offset – десяткове число. Однак, зломщик може спробувати зламати систему, приєднавши до URL наступне значення:

0; insert into pg\_shadow(usename,usesysid,usesuper,usecatupd,passwd) select 'crack', usesysid, 't','t','crack' from pg\_shadow where usename='postgres'; --

Якщо це станеться, скрипт надасть зловмиснику доступ суперкористувача. Зверніть увагу, що значення `0;` використано для того, щоб задати правильне усунення першого запиту і коректно його завершити.

> **Зауваження** :
> 
> Це поширений прийом, щоб змусити синтаксичний аналізатор SQL ігнорувати решту запиту, написаного розробником за допомогою `--`який є знаком коментаря в SQL.

Ще один можливий спосіб отримати паролі облікових записів у БД – атака сторінок, що надають пошук по базі. Зловмиснику потрібно лише перевірити, чи використовується в запиті змінна, що передається на сервер і необроблена належним чином. Це може бути один із фільтрів, що встановлюються на попередній сторінці, таких як `WHERE, ORDER BY, LIMIT`и`OFFSET`, що використовуються при побудові запитів `SELECT`. У випадку, якщо база даних, що використовується вами, підтримує конструкцію `UNION`, зловмисник може приєднати до оригінального запиту ще один додатковий, для вилучення паролів користувача. Рекомендуємо використовувати тільки зашифровані паролі.

**Приклад #2 Лістинг статей... та деяких паролів (для будь-якої бази даних)**

```php
<?php

$query  = "SELECT id, name, inserted, size FROM products
         WHERE size = '$size'";
$result = odbc_exec($conn, $query);
?>
```

Статична частина запиту може комбінуватись з іншим `SELECT`\-запит, який виведе всі паролі:

'

## union select '1', concat(uname||'-'||passwd) as name, '1971-01-01', '0' from usertable;

Вирази `UPDATE`и`INSERT` також схильні до таких атак.

**Приклад #3 Від скидання пароля до отримання додаткових привілеїв (будь-який сервер баз даних)**

```php
<?php
$query = "UPDATE usertable SET pwd='$pwd' WHERE uid='$uid';";
?>
```

Але зловмисник може ввести значення `' or uid like'%admin%'` для змінної $uid для зміни пароля адміністратора або просто присвоїти змінної $pwd значення `hehehe', trusted=100, admin='yes` для отримання додаткових привілеїв. При виконанні запити переплітаються:

```php
<?php

// $uid: ' or uid like '%admin%
$query = "UPDATE usertable SET pwd='...' WHERE uid='' or uid like '%admin%';";

// $pwd: hehehe', trusted=100, admin='yes
$query = "UPDATE usertable SET pwd='hehehe', trusted=100, admin='yes' WHERE
...;";
?>
```

Хоча залишається очевидним, що для проведення успішної атаки зловмисник повинен мати хоча б деякі знання про архітектуру бази даних, отримати цю інформацію дуже просто. Наприклад, код може бути частиною програмного забезпечення з відкритим вихідним кодом і перебувати у відкритому доступі. Ця інформація також може бути розкрита закритим кодом - навіть якщо він закодований, обфусцьований або скомпільований, і навіть вашим власним кодом через відображення повідомлень про помилки. Інші методи включають використання типових імен таблиць та стовпців. Наприклад, форма входу в систему, яка використовує таблицю 'users' з іменами стовпців 'id', 'username' та 'password'.

**Приклад #4 Атака на операційну систему сервера бази даних (MSSQL Server)**

Жахливий приклад того, як команди рівня операційної системи можуть бути доступні на деяких вузлах баз даних.

```php
<?php

$query  = "SELECT * FROM products WHERE id LIKE '%$prod%'";
$result = mssql_query($query);
?>
```

Якщо зловмисник передасть значення `a%' exec master..xp_cmdshell 'net user test testpass /ADD' --` в $prod, $query буде:

```php
<?php

$query  = "SELECT * FROM products
         WHERE id LIKE '%a%'
         exec master..xp_cmdshell 'net user test testpass /ADD' --%'";
$result = mssql_query($query);
?>
```

MSSQL Server виконує SQL запити в пакеті, включаючи команду додавання нового користувача до локальної бази даних облікових записів. Якби ця програма була запущена від імені `sa` і служба MSSQLSERVER була запущена з достатніми привілеями, у зловмисника з'явився обліковий запис, за допомогою якого він міг би отримати доступ до цієї машини.

> **Зауваження** :
> 
> Деякі приклади, наведені вище, прив'язані до конкретного серверу баз даних, але це не означає, що подібна атака неможлива на інші продукти. Ваш сервер баз даних може бути аналогічно вразливим та іншим способом.

![Забавний приклад проблем, пов'язаних із SQL-ін'єкціями](images/fa7c5b5f326e3c4a6cc9db19e7edbaf0-xkcd-bobby-tables.png)

Изображение любезно предоставлено[» xkcd](http://xkcd.com/327)

### Способи захисту

Рекомендований спосіб уникнути SQL-ін'єкцій – зв'язування всіх даних за допомогою підготовлених запитів. Використання підготовлених запитів недостатньо для повного запобігання SQL-ін'єкцій, але це найпростіший і найбезпечніший спосіб забезпечити введення даних у SQL-запити. Усі динамічні літерали даних у виразах `WHERE` `SET`и`VALUES` мають бути замінені заповнювачами. Фактичні дані будуть пов'язані під час виконання та надіслані окремо від команди SQL.

Прив'язка параметрів може використовуватись лише для даних. Інші динамічні частини SQL-запиту мають бути відфільтровані за відомим списком допустимих значень.

**Приклад #5 Уникнення SQL-ін'єкцій за допомогою підготовлених операторів PDO**

```php
<?php

// Динамическая часть SQL проверяется на соответствие ожидаемым значениям
$sortingOrder = $_GET['sortingOrder'] === 'DESC' ? 'DESC' : 'ASC';
$productId = $_GET['productId'];

// SQL подготавливается с заполнителем
$stmt = $pdo->prepare("SELECT * FROM products WHERE id LIKE ? ORDER BY price {$sortingOrder}");

// Значение предоставляется с подстановочными знаками LIKE
$stmt->execute(["%{$productId}%"]);
?>
```

Підготовлені оператори надаються [PDO](pdo.prepared-statements.md) [MySQLi](mysqli.quickstart.prepared-statements.md), а також іншими бібліотеками баз даних.

Атаки SQL-ін'єкцій в основному засновані на використанні коду, написаного без урахування вимог безпеки. Ніколи не довіряйте будь-якому введенню, особливо з боку клієнта, навіть якщо він надходить із поля вибору, прихованого поля введення або cookie. Перший приклад показує, що такий простий запит може спричинити катастрофу.

Стратегія "захист у глибину" включає кілька ефективних методів написання коду:

-   Ніколи не підключайтеся до бази даних як суперкористувач або власник бази даних. Завжди використовуйте налаштованих користувачів із мінімальними привілеями.
-   Завжди перевіряйте введені дані на відповідність очікуваного типу. У PHP є безліч функцій для перевірки даних: починаючи від найпростіших[функцій для роботи зі змінними](ref.var.md) і [функцій визначення типу символів](ref.ctype.md)(таких як[is\_numeric()](function.is-numeric.md) і [ctype\_digit()](function.ctype-digit.md)відповідно) та закінчуючи[Perl-сумісними регулярними виразами](ref.pcre.md)
-   У випадку, якщо програма очікує цифрове введення, застосуйте функцію[ctype\_digit()](function.ctype-digit.md)для перевірки введених даних, або примусово вкажіть їх тип за допомогою[settype()](function.settype.md), або просто використовуйте числове подання за допомогою функції[sprintf()](function.sprintf.md)
-   Якщо на рівні бази даних не підтримуються прив'язані змінні, то завжди екрануйте будь-які нечислові дані, які використовуються в запитах до БД за допомогою спеціальних функцій, що екранують, специфічних для використовуваної вами бази даних (наприклад,[mysql\_real\_escape\_string()](function.mysql-real-escape-string.md) \*\*sqlite\_escape\_string()\*\*і т.д.). Загальні функції, такі як[addslashes()](function.addslashes.md)корисні лише у певних випадках (наприклад MySQL в однобайтному кодуванні з вимкненим NO\_BACKSLASH\_ESCAPES), тому краще уникати їх використання.
-   У жодному разі не виводьте жодної інформації про БД, особливо про її структуру. Також ознайомтесь із відповідними розділами документації: " [Повідомлення про помилки](security.errors.md) "і"[Функції обробки та логування помилок](ref.errorfunc.md)".

Крім того, ви можете логувати запити у вашому скрипті або на рівні бази даних, якщо вона це підтримує. Очевидно, що логування не може запобігти завданню шкоди, але може допомогти при трасуванні зламаної програми. Лог-файл корисний не сам собою, а інформацією, яка в ньому міститься. Причому, як правило, корисно логувати всі можливі деталі.
