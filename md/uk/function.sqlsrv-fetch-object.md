---
navigation:
  - function.sqlsrv-fetch-array.md: « sqlsrvfetcharray
  - function.sqlsrv-fetch.md: sqlsrvfetch »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrvfetchobject
---
# sqlsrvfetchobject

(No version information available, might only be in Git)

sqlsrvfetchobject — Отримує наступний рядок даних у наборі результатів як об'єкт

### Опис

```methodsynopsis
sqlsrv_fetch_object(    resource $stmt,    string $className = ?,    array $ctorParams = ?,    int $row = ?,    int $offset = ?): mixed
```

Витягує наступний рядок даних у наборі результатів як екземпляр зазначеного класу з властивостями, що відповідають іменам полів рядка та значенням, що відповідають значенням полів рядка.

### Список параметрів

`stmt`

Ресурс оператора, що повертається [sqlsrvquery()](function.sqlsrv-query.md) або [sqlsrvexecute()](function.sqlsrv-execute.md)

`className`

Назва класу для створення екземпляра. Якщо ім'я класу не вказано, створюється екземпляр stdClass.

`ctorParams`

Значення, що передаються конструктору зазначеного класу. Якщо конструктор зазначеного класу приймає параметри, необхідно надати масив ctorParams.

`row`

Рядок, до якого потрібно отримати доступ. Параметр можна використовувати лише в тому випадку, якщо вказаний оператор був підготовлений за допомогою курсору з можливістю прокручування. У цьому випадку цей параметр може приймати одне з таких значень:

-   SQLSRVSCROLLNEXT
-   SQLSRVSCROLLPRIOR
-   SQLSRVSCROLLFIRST
-   SQLSRVSCROLLLAST
-   SQLSRVSCROLLABSOLUTE
-   SQLSRVSCROLLRELATIVE

`offset`

Вказує рядок, до якого буде доступ, якщо для параметра рядка встановлено значення **`SQLSRV_SCROLL_ABSOLUTE`** або **`SQLSRV_SCROLL_RELATIVE`**. Зауважте, що перший рядок у наборі результатів має індекс 0.

### Значення, що повертаються

У разі успішного виконання повертає об'єкт, \*\*`null`\*\*якщо в наборі результатів більше немає рядків і **`false`** у разі виникнення помилки або якщо зазначений клас не існує.

### Приклади

**Приклад #1 Приклад використання **sqlsrvfetchobject()****

У цьому прикладі показано, як отримати рядок як об'єкт stdClass.

```php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

$sql = "SELECT fName, lName FROM Table_1";
$stmt = sqlsrv_query( $conn, $sql);
if( $stmt === false ) {
     die( print_r( sqlsrv_errors(), true));
}

// Получение каждой строки как объект.
// Поскольку класс не указан, каждая строка будет получена как объект stdClass.
// Имена свойств соответствуют именам полей.
while( $obj = sqlsrv_fetch_object( $stmt)) {
      echo $obj->fName.", ".$obj->lName."<br />";
}
?>
```

### Примітки

Якщо ім'я класу вказано з необов'язковим параметром $className і клас має властивості, імена яких збігаються з іменами полів набору результатів, до властивостей застосовуються відповідні значення набору результатів. Якщо ім'я поля набору результатів не відповідає властивості класу, властивість з ім'ям поля набору результатів додається до об'єкта, а значення набору результатів застосовується до властивості. При використанні параметра $className застосовуються такі правила:

-   При зіставленні імен властивостей поля враховується регістр.
-   Порівняння властивостей поля відбувається незалежно від модифікаторів доступу.
-   Типи даних властивостей класу ігноруються при застосуванні значення поля властивості.
-   Якщо клас немає, функція повертає **`false`** та додає помилку до колекції помилок.

Незалежно від того, чи вказано параметр $className, якщо поле повертається без імені, значення поля буде проігноровано, а до колекції помилок буде додано попередження.

При використанні набору результатів, що містить кілька стовпців з однаковим ім'ям, можливо краще використовувати [sqlsrvfetcharray()](function.sqlsrv-fetch-array.md) або комбінацію [sqlsrvfetch()](function.sqlsrv-fetch.md) і [sqlsrvgetfield()](function.sqlsrv-get-field.md)

### Дивіться також

-   [sqlsrvfetch()](function.sqlsrv-fetch.md) - Робить наступний рядок у наборі результатів доступного для читання
-   [sqlsrvfetcharray()](function.sqlsrv-fetch-array.md) - Повертає рядок як масив
