Встановлює нове з'єднання із сервером Oracle

-   [« ocinewcollection](function.oci-new-collection.html)
    
-   [ocinewcursor »](function.oci-new-cursor.html)
    
-   [PHP Manual](index.md)
    
-   [OCI8 Функции](ref.oci8.md)
    
-   Встановлює нове з'єднання із сервером Oracle
    

# ocinewconnect

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocinewconnect — Встановлює нове з'єднання із сервером Oracle

### Опис

```methodsynopsis
oci_new_connect(    string $username,    string $password,    ?string $connection_string = null,    string $encoding = "",    int $session_mode = OCI_DEFAULT): resource|false
```

Створює нове з'єднання з сервером Oracle та здійснює вхід.

На відміну від [ociconnect()](function.oci-connect.html) і [ocipconnect()](function.oci-pconnect.html), функція **ocinewconnect()** не кешує з'єднання і під час кожного виклику встановлює нове з'єднання. Це корисно, якщо додатку потрібна транзакційна ізоляція двох наборів запитів.

### Список параметрів

`username`

Ім'я користувача Oracle.

`password`

Пароль користувача `username`

`connection_string`

Містить `экземпляр Oracle` для підключення. Це може бути [» Easy Connect string](https://www.oracle.com/pls/topic/lookup?ctx=dblatest&id=GUID-E5358DEA-D619-4B7B-A799-3D2F802500F1), або Connect Name з файлу tnsnames.ora, або ім'я локального екземпляра Oracle.

Якщо не вказано окремо або **`null`**, PHP використовує змінні оточення, такі як **`TWO_TASK`** (на Linux) або **`LOCAL`** (на Windows) та **`ORACLE_SID`** для визначення `экземпляра Oracle` для з'єднання.

Для використання методу Easy Connect, PHP має бути з'єднаний з клієнтськими бібліотеками версії Oracle 10*г* чи старше. Easy Connect string для Oracle 10*г* приймає таку форму: *hostname:port/servicename*. Починаючи з Oracle 11*г* синтаксис такий: *hostname:port/servicename:servertype/instancename*. У Oracle 19c було введено додаткові параметри, включаючи налаштування часу очікування та перевірки активності. Зверніться до документації Oracle. Назви служб можуть бути визначені за допомогою запуску Oracle утиліти `lsnrctl status` на сервері бази даних.

Файл tnsnames.ora може знаходитись у пошуковому шляху Oracle Net, який включає /your/path/to/instantclient/network/admin, $ORACLEHOME/network/admin та /etc. Як альтернативний варіант можна встановити `TNS_ADMIN` таким чином, щоб шлях $TNSADMIN/tnsnames.ora читав. Переконайтеся, що веб-сервер має доступ до файлу.

`encoding`

Визначає кодування, яке використовується клієнтськими бібліотеками Oracle. Дане кодування не обов'язково має збігатися з кодуванням, яке використовується в самій базі даних. Якщо вона не збігається, Oracle зробить все можливе для конвертування даних із-і в дане кодування. Залежно від використовуваних кодувань, це може не завжди давати прийнятні результати. Перетворення також створює деякі додаткові витрати часу.

Якщо кодування не вказано, клієнтські бібліотеки Oracle визначатимуть його зі змінного оточення. **`NLS_LANG`**

Передача цього параметра може зменшити час, що витрачається на з'єднання.

`session_mode`

Цей параметр доступний починаючи з версії PHP 5 (PECL OCI8 1.1) і набуває наступних значень: **`OCI_DEFAULT`** **`OCI_SYSOPER`** і **`OCI_SYSDBA`**. Якщо було вказано **`OCI_SYSOPER`** або **`OCI_SYSDBA`**, дана функція спробує встановити привілейоване з'єднання, використовуючи зовнішні дані авторизації. За замовчуванням привілейовані з'єднання вимкнено. Щоб їх увімкнути, необхідно встановити [oci8.privilegedconnect](oci8.configuration.html#ini.oci8.privileged-connect) в `On`

У версії PHP 5.3 (PECL OCI8 1.3.4) з'явилося значення **`OCI_CRED_EXT`**. Воно вказує Oracle використовувати зовнішню автентифікацію або автентифікацію за допомогою операційної системи, що має бути налаштовано у базі даних. Прапор **`OCI_CRED_EXT`** може бути використаний тільки з ім'ям користувача "/" та порожнім паролем . [oci8.privilegedconnect](oci8.configuration.html#ini.oci8.privileged-connect) може набувати значення `On` або `Off`

**`OCI_CRED_EXT`** може використовуватися спільно з режимами **`OCI_SYSOPER`** і **`OCI_SYSDBA`**

**`OCI_CRED_EXT`** не підтримується у Windows через безпеку.

### Значення, що повертаються

Повертає ідентифікатор з'єднання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | `connection_string` тепер допускає значення null. |

### Приклади

Наведений нижче приклад ілюструє використання відокремлених сполук.

**Приклад #1 Приклад використання **ocinewconnect()****

```php
<?php

// создайте таблицу mytab (mycol number);

function query($name, $c)
{
    echo "Выполнение $name\n";
    $s = oci_parse($c, "select * from mytab");
    oci_execute($s, OCI_NO_AUTO_COMMIT);
    $row = oci_fetch_array($s, OCI_ASSOC);
    if (!$row) {
        echo "Нет данных\n";
    } else {
        do {
            foreach ($row as $item)
                echo $item . " ";
            echo "\n";
        } while (($row = oci_fetch_array($s, OCI_ASSOC)) != false);
    }
}

$c1 = oci_connect("hr", "welcome", "localhost/orcl");
$c2 = oci_new_connect("hr", "welcome", "localhost/orcl");

$s = oci_parse($c1, "insert into mytab values(1234)");
oci_execute($s, OCI_NO_AUTO_COMMIT);

query("основного соединения", $c1);
query("нового соединения", $c2);
oci_commit($c1);
query("нового соединения после commit", $c2);

// Выведет:
//   Выполнение основного соединения
//   1234
//   Выполнение нового соединения
//   Нет данных
//   Выполнение нового соединения после commit
//   1234

?>
```

Додаткові приклади можна знайти в описі функції [ociconnect()](function.oci-connect.html)

### Дивіться також

-   [ociconnect()](function.oci-connect.html) - Встановлює з'єднання з базою даних Oracle
-   [ocipconnect()](function.oci-pconnect.html) - Встановлює постійне з'єднання із сервером Oracle