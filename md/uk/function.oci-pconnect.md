---
navigation:
  - function.oci-password-change.md: « oci\_password\_change
  - function.oci-register-taf-callback.md: oci\_register\_taf\_callback »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_pconnect
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_pconnect

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

oci\_pconnect — Встановлює постійне з'єднання із сервером Oracle

### Опис

```methodsynopsis
oci_pconnect(    string $username,    string $password,    ?string $connection_string = null,    string $encoding = "",    int $session_mode = OCI_DEFAULT): resource|false
```

Створює постійне з'єднання з сервером Oracle та виконує аутентифікацію.

Постійні з'єднання кешуються та повторно використовуються при наступних запитах, в результаті знижуються накладні витрати при кожному завантаженні сторінки; Типова програма PHP має одне постійне підключення до сервера PHP, реалізоване дочірнім процесом Apache (або процесом PHP FPM). Додаткову інформацію дивіться у розділі [Робота зі з'єднаннями OCI8 та Connection Pooling](oci8.connection.md)

### Список параметрів

`username`

Ім'я користувача Oracle.

`password`

Пароль користувача `username`

`connection_string`

Містить `екземпляр Oracle` для підключення. Це може бути [» Easy Connect string](https://www.oracle.com/pls/topic/lookup?ctx=dblatest&id=GUID-E5358DEA-D619-4B7B-A799-3D2F802500F1), або Connect Name з файлу tnsnames.ora, або ім'я локального екземпляра Oracle.

Якщо не вказано окремо або **`null`**, PHP використовує змінні оточення, такі як **`TWO_TASK`**(на Linux) или\*\*`LOCAL`**(на Windows) и**`ORACLE_SID`\*\*для определения`екземпляра Oracle`для соединения.

Для використання методу Easy Connect, PHP має бути з'єднаний з клієнтськими бібліотеками версії Oracle 10*g*или старше. Easy Connect string для Oracle 10*g*принимает следующую форму:*\[//\]host\_name\[:port\]\[/service\_name\]*. Починаючи з Oracle 11*g* синтаксис такий: *\[//\]host\_name\[:port\]\[/service\_name\]\[:server\_type\]\[/instance\_name\]*. У Oracle 19c було введено додаткові параметри, включаючи налаштування часу очікування та перевірки активності. Зверніться до документації Oracle. Назви служб можуть бути визначені за допомогою запуску Oracle утиліти `lsnrctl status` на сервері бази даних.

Файл tnsnames.ora може знаходитись у пошуковому шляху Oracle Net, який включає /your/path/to/instantclient/network/admin, $ORACLE\_HOME/network/admin та /etc. Як альтернативний варіант можна встановити `TNS_ADMIN` таким чином, щоб шлях $TNS\_ADMIN/tnsnames.ora читав. Переконайтеся, що веб-сервер має доступ до файлу.

`encoding`

Визначає кодування, яке використовуватимуть клієнтські бібліотеки Oracle. Це кодування не обов'язково має збігатися з кодуванням, яке використовується в самій базі даних. Якщо вона не збігається, Oracle зробить все можливе для конвертування даних з-і в це кодування. Залежно від використовуваних кодувань, це може не завжди давати прийнятні результати. Перетворення також створює деякі додаткові витрати часу.

Якщо кодування не вказано, клієнтські бібліотеки Oracle будуть визначати його зі змінного оточення. **`NLS_LANG`**

Передача цього параметра може зменшити час, що витрачається на з'єднання.

`session_mode`

Цей параметр доступний починаючи з версії PHP 5 (PECL OCI8 1.1) і набуває наступних значень: **`OCI_DEFAULT`** **`OCI_SYSOPER`** і **`OCI_SYSDBA`**. Якщо були вказані \*\*`OCI_SYSOPER`** або **`OCI_SYSDBA`\*\*ця функція спробує встановити привілейоване з'єднання, використовуючи зовнішні дані авторизації. За замовчуванням привілейовані з'єднання вимкнено. Щоб їх увімкнути, необхідно встановити [oci8.privileged\_connect](oci8.configuration.md#ini.oci8.privileged-connect)в`On`

У версії PHP 5.3 (PECL OCI8 1.3.4) з'явилося значення **`OCI_CRED_EXT`**. Воно вказує Oracle використовувати зовнішню автентифікацію або автентифікацію за допомогою операційної системи, що має бути налаштовано у базі даних. Прапор **`OCI_CRED_EXT`** може бути використаний лише з ім'ям користувача "/" та порожнім паролем. . [oci8.privileged\_connect](oci8.configuration.md#ini.oci8.privileged-connect) може набувати значення `On`или`Off`

**`OCI_CRED_EXT`** може використовуватися спільно з режимами **`OCI_SYSOPER`** і **`OCI_SYSDBA`**

**`OCI_CRED_EXT`** не підтримується у Windows через безпеку.

### Значення, що повертаються

Повертає ідентифікатор підключення або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Простий приклад для **oci\_pconnect()** з використанням спрощеного синтаксису підключення**

```php
<?php

// Подключение к XE сервису (т.е. базе данных) на локальной машине
$conn = oci_pconnect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'SELECT * FROM employees');
oci_execute($stid);

echo "<table border='1'>\n";
while ($row = oci_fetch_array($stid, OCI_ASSOC+OCI_RETURN_NULLS)) {
    echo "<tr>\n";
    foreach ($row as $item) {
        echo "    <td>" . ($item !== null ? htmlentities($item, ENT_QUOTES) : "") . "</td>\n";
    }
    echo "</tr>\n";
}
echo "</table>\n";

?>
```

Додаткові приклади можна знайти в описі функції [oci\_connect()](function.oci-connect.md)

### Примітки

> **Зауваження**: Тривалість та максимальна кількість постійних з'єднань до сервера Oracle на кожен процес PHP може бути змінена в наступних директивах: [oci8.persistent\_timeout](oci8.configuration.md#ini.oci8.persistent-timeout) [oci8.ping\_interval](oci8.configuration.md#ini.oci8.ping-interval) і [oci8.max\_persistent](oci8.configuration.md#ini.oci8.max-persistent)

### Дивіться також

-   [oci\_connect()](function.oci-connect.md) \- Встановлює з'єднання з базою даних Oracle
-   [oci\_new\_connect()](function.oci-new-connect.md) \- Встановлює нове з'єднання із сервером Oracle
