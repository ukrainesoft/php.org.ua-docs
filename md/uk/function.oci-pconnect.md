---
navigation:
  - function.oci-password-change.html: « ocipasswordchange
  - function.oci-register-taf-callback.html: ociregistertafcallback »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функции
title: ocipconnect
---
# ocipconnect

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocipconnect — Встановлює постійне з'єднання із сервером Oracle

### Опис

```methodsynopsis
oci_pconnect(    string $username,    string $password,    ?string $connection_string = null,    string $encoding = "",    int $session_mode = OCI_DEFAULT): resource|false
```

Створює постійне з'єднання з сервером Oracle та виконує аутентифікацію.

Постійні з'єднання кешуються та повторно використовуються при наступних запитах, в результаті знижуються накладні витрати при кожному завантаженні сторінки; Типова програма PHP має одне постійне підключення до сервера PHP, реалізоване дочірнім процесом Apache (або процесом PHP FPM). Додаткову інформацію дивіться у розділі [Работа с соединениями OCI8 и Connection Pooling](oci8.connection.md)

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

Цей параметр доступний починаючи з версії PHP 5 (PECL OCI8 1.1) і набуває наступних значень: **`OCI_DEFAULT`** **`OCI_SYSOPER`** і **`OCI_SYSDBA`**. Якщо були вказані **`OCI_SYSOPER`** або **`OCI_SYSDBA`**, дана функція спробує встановити привілейоване з'єднання, використовуючи зовнішні дані авторизації. За замовчуванням привілейовані з'єднання вимкнено. Щоб їх увімкнути, необхідно встановити [oci8.privilegedconnect](oci8.configuration.html#ini.oci8.privileged-connect) в `On`

У версії PHP 5.3 (PECL OCI8 1.3.4) з'явилося значення **`OCI_CRED_EXT`**. Воно вказує Oracle використовувати зовнішню автентифікацію або автентифікацію за допомогою операційної системи, що має бути налаштовано у базі даних. Прапор **`OCI_CRED_EXT`** може бути використаний тільки з ім'ям користувача "/" та порожнім паролем . [oci8.privilegedconnect](oci8.configuration.html#ini.oci8.privileged-connect) може набувати значення `On` або `Off`

**`OCI_CRED_EXT`** може використовуватися спільно з режимами **`OCI_SYSOPER`** і **`OCI_SYSDBA`**

**`OCI_CRED_EXT`** не підтримується у Windows через безпеку.

### Значення, що повертаються

Повертає ідентифікатор підключення або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Простий приклад для **ocipconnect()** з використанням спрощеного синтаксису підключення**

```php
<?php

// Подключение к XE сервису (т.е. базе данных) на локальной машине
$conn = oci_pconnect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'SELECT * FROM employees');
oci_execute($stid);

echo "<table border='1'>\n";
while ($row = oci_fetch_array($stid, OCI_ASSOC+OCI_RETURN_NULLS)) {
    echo "<tr>\n";
    foreach ($row as $item) {
        echo "    <td>" . ($item !== null ? htmlentities($item, ENT_QUOTES) : "") . "</td>\n";
    }
    echo "</tr>\n";
}
echo "</table>\n";

?>
```

Додаткові приклади можна знайти в описі функції [ociconnect()](function.oci-connect.html)

### Примітки

> **Зауваження**: Починаючи з версії PHP 5.1.2 та PECL OCI8 1.1, тривалість та максимальна кількість постійних з'єднань до сервера Oracle на кожен процес PHP може бути змінена в наступних директивах: [oci8.persistenttimeout](oci8.configuration.html#ini.oci8.persistent-timeout) [oci8.pinginterval](oci8.configuration.html#ini.oci8.ping-interval) і [oci8.maxpersistent](oci8.configuration.html#ini.oci8.max-persistent)

### Дивіться також

-   [ociconnect()](function.oci-connect.html) - Встановлює з'єднання з базою даних Oracle
-   [ocinewconnect()](function.oci-new-connect.html) - Встановлює нове з'єднання із сервером Oracle
