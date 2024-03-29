---
navigation:
  - class.pdostatement.md: « PDOStatement
  - pdostatement.bindparam.md: 'PDOStatement::bindParam »'
  - index.md: PHP Manual
  - class.pdostatement.md: PDOStatement
title: 'PDOStatement::bindColumn'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDOStatement::bindColumn

(PHP 5 >= 5.1.0, PHP 7, PHP 8, PECL pdo >= 0.1.0)

PDOStatement::bindColumn — Зв'язує стовпець зі змінною PHP

### Опис

```methodsynopsis
public PDOStatement::bindColumn(    string|int $column,    mixed &$var,    int $type = PDO::PARAM_STR,    int $maxLength = 0,    mixed $driverOptions = null): bool
```

**PDOStatement::bindColumn()** прив'язує змінну до заданого стовпця у результуючому наборі запиту. Кожен виклик [PDOStatement::fetch()](pdostatement.fetch.md) або [PDOStatement::fetchAll()](pdostatement.fetchall.md) оновлюватиме всі змінні, задаватиме їм значення стовпців, з якими вони пов'язані.

> **Зауваження** :
> 
> У зв'язку з тим, що інформація про стовпці результуючого набору запиту не завжди доступна об'єкту PDO, поки запит не буде запущений, додаткам слід викликати цей метод *після* виклику [PDOStatement::execute()](pdostatement.execute.md)
> 
> Однако, при работе с*драйвером PgSQL*, коли прив'язується стовпець з LOB-даними, додатком необхідно викликати цей метод *до* виклику [PDOStatement::execute()](pdostatement.execute.md). В іншому випадку ідентифікатор великого об'єкта OID матиме тип integer.

### Список параметрів

`column`

Номер стовпця (починаючи з 1) або його ім'я у результуючому наборі запиту. Використовуючи ім'я стовпця, майте на увазі, що ім'я має бути в тому ж регістрі, в якому воно повернуто драйвером.

`var`

Ім'я змінної PHP, до якої потрібно прив'язати стовпець.

`type`

Тип даних параметра, заданий однією з констант [`PDO::PARAM_*`](pdo.constants.md)

`maxLength`

Підказка для попереднього виділення пам'яті під змінну.

`driverOptions`

Додаткові параметри драйвера.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Видає помилку рівня **`E_WARNING`**, якщо атрибуту **`PDO::ATTR_ERRMODE`**установлено значение**`PDO::ERRMODE_WARNING`**

Викидає виняток [PDOException](class.pdoexception.md), якщо атрибуту **`PDO::ATTR_ERRMODE`**установлено значение**`PDO::ERRMODE_EXCEPTION`**

### Приклади

**Приклад #1 Зв'язування результуючого набору зі змінними PHP**

Прив'язування стовпців результуючого набору до PHP змінним є ефективним способом відразу зробити дані кожного рядка набору доступними додатком. У наступному прикладі показано, як PDO дозволяє прив'язувати змінні та отримувати дані стовпців, приймаючи різні налаштування та замовчування.

```php
<?php
$stmt = $dbh->prepare('SELECT name, colour, calories FROM fruit');
$stmt->execute();

/* Bind by column number */
$stmt->bindColumn(1, $name);
$stmt->bindColumn(2, $colour);

/* Bind by column name */
$stmt->bindColumn('calories', $cals);

while ($stmt->fetch(PDO::FETCH_BOUND)) {
    print $name . "\t" . $colour . "\t" . $cals . "\n";
}
```

Результат виконання наведеного прикладу:

```
apple   red     150
banana  yellow  175
kiwi    green   75
orange  orange  150
mango   red     200
strawberry      red     25
```

### Дивіться також

-   [PDOStatement::execute()](pdostatement.execute.md) \- Запускає підготовлений запит на виконання
-   [PDOStatement::fetch()](pdostatement.fetch.md) \- Вилучення наступного рядка з результуючого набору
-   [PDOStatement::fetchAll()](pdostatement.fetchall.md) \- Вибирає рядки, що залишилися, з набору результатів
-   [PDOStatement::fetchColumn()](pdostatement.fetchcolumn.md) \- Повертає дані одного стовпця наступного рядка результуючого набору
