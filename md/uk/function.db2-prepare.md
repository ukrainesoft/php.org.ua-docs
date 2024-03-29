---
navigation:
  - function.db2-pconnect.md: « db2\_pconnect
  - function.db2-primary-keys.md: db2\_primary\_keys »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2\_prepare
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# db2\_prepare

(PECL ibm\_db2 >= 1.0.0)

db2\_prepare — Підготовка SQL-запиту до виконання

### Опис

```methodsynopsis
db2_prepare(resource $connection, string $statement, array $options = []): resource|false
```

**db2\_prepare()** створює підготовлений SQL-запит, який може містити 0 або більше маркерів параметрів (символів `?` ), що представляють вхідні параметри, параметри виведення або вхідні параметри та параметри виведення. Ви можете передати параметри підготовленому запиту за допомогою [db2\_bind\_param()](function.db2-bind-param.md) або тільки для вхідних значень у вигляді масиву, переданого в [db2\_execute()](function.db2-execute.md)

Використання підготовлених запитів у вашому додатку дає три основні переваги:

-   *Продуктивність*: при використанні підготовленого запиту сервер бази даних створює оптимізований план доступу для вилучення даних за допомогою цього запиту. Подальше виконання підготовленого запиту за допомогою[db2\_execute()](function.db2-execute.md)дозволяє операторам повторно використовувати цей план доступу і дозволяє уникнути накладних витрат на динамічне створення нового плану доступу для кожного запиту, який ви виконуєте.
    
-   *Безпека* : під час використання підготовленого запиту можна ввімкнути маркери параметрів для вхідних значень. Коли ви виконуєте підготовлений запит із вхідними значеннями для заповнювачів, сервер бази даних перевіряє кожне вхідне значення, щоб переконатися, що тип відповідає визначенню стовпця або параметру.
    
-   *Розширений функціонал*: Маркери параметрів не тільки дозволяють передавати вхідні значення в підготовлені SQL-запити, вони також дозволяють витягувати параметри OUT і INOUT зі збережених процедур за допомогою[db2\_bind\_param()](function.db2-bind-param.md)
    

### Список параметрів

`connection`

Допустима змінна ресурсу підключення до бази даних, що повертається функцією [db2\_connect()](function.db2-connect.md) або [db2\_pconnect()](function.db2-pconnect.md)

`statement`

SQL-запит, який необов'язково містить один або кілька маркерів параметрів.

`options`

Асоціативний масив містить параметри запиту. Параметри можна використовувати для запиту курсору, що прокручується, на серверах баз даних, що підтримують цю функцію.

Опис допустимих опцій запиту дивіться у розділі [db2\_set\_option()](function.db2-set-option.md)

### Значення, що повертаються

Повертає ресурс оператора, якщо SQL-запит було успішно проаналізовано та підготовлено сервером бази даних. Повертає \*\*`false`\*\*якщо сервер бази даних повернув помилку. Ви можете визначити, яка помилка була повернена, викликавши [db2\_stmt\_error()](function.db2-stmt-error.md) або [db2\_stmt\_errormsg()](function.db2-stmt-errormsg.md)

### Приклади

**Приклад #1 Підготовка та виконання SQL-запиту з маркерами параметрів**

У наступному прикладі готується запит INSERT, який приймає чотири маркери параметрів, а потім виконує ітерацію масивів, що містять вхідні значення, які необхідно передати в [db2\_execute()](function.db2-execute.md)

```php
<?php
$animals = array(
    array(0, 'cat', 'Pook', 3.2),
    array(1, 'dog', 'Peaches', 12.3),
    array(2, 'horse', 'Smarty', 350.0),
);

$insert = 'INSERT INTO animals (id, breed, name, weight)
    VALUES (?, ?, ?, ?)';
$stmt = db2_prepare($conn, $insert);
if ($stmt) {
    foreach ($animals as $animal) {
        $result = db2_execute($stmt, $animal);
    }
}
?>
```

### Дивіться також

-   [db2\_bind\_param()](function.db2-bind-param.md) \- Зв'язує змінну PHP із параметром SQL-виразу
-   [db2\_execute()](function.db2-execute.md) \- Виконує підготовлений SQL-запит
-   [db2\_stmt\_error()](function.db2-stmt-error.md) \- Повертає рядок, що містить SQLSTATE, повернутий SQL-оператором
-   [db2\_stmt\_errormsg()](function.db2-stmt-errormsg.md) \- Повертає рядок, що містить останнє повідомлення про помилку SQL-виразу
