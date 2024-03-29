---
navigation:
  - pdo.rollback.md: '« PDO::rollBack'
  - class.pdostatement.md: PDOStatement »
  - index.md: PHP Manual
  - class.pdo.md: PDO
title: 'PDO::setAttribute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDO::setAttribute

(PHP 5 >= 5.1.0, PHP 7, PHP 8, PECL pdo >= 0.1.0)

PDO::setAttribute — Встановлення атрибуту

### Опис

```methodsynopsis
public PDO::setAttribute(int $attribute, mixed $value): bool
```

Встановлює атрибут об'єкта PDO. Деякі основні атрибути наведені нижче; окремі драйвери можуть використовувати додаткові атрибути. Зверніть увагу, що атрибути драйвера *не повинні* використовуватись з іншими драйверами.

**`PDO::ATTR_CASE`**

Примусове приведення імен шпальт до певного регістру. Може приймати одне з таких значень:

**`PDO::CASE_LOWER`**

Примусове приведення імен шпальт до нижнього регістру.

**`PDO::CASE_NATURAL`**

Залишити імена шпальт у тому вигляді, в якому їх повертає драйвер бази даних.

**`PDO::CASE_UPPER`**

Примусове приведення імен шпальт до верхнього регістру.

**`PDO::ATTR_ERRMODE`**

Режим повідомлення про помилки PDO. Може приймати одне з таких значень:

**`PDO::ERRMODE_SILENT`**

Встановлює лише коди помилок.

**`PDO::ERRMODE_WARNING`**

Викликає діагностику помилок рівня **`E_WARNING`**

**`PDO::ERRMODE_EXCEPTION`**

Викидає [PDOException](class.pdoexception.md)

**`PDO::ATTR_ORACLE_NULLS`**

> **Зауваження**: Атрибут доступний для всіх драйверів, а не для Oracle.

Визначає, чи слід і як перетворювати **`null`** та порожні рядки. Може приймати одне з таких значень:

**`PDO::NULL_NATURAL`**

Жодного перетворення не відбувається.

**`PDO::NULL_EMPTY_STRING`**

Порожні рядки перетворюються на **`null`**

**`PDO::NULL_TO_STRING`**

\*\*`null`\*\*преобразуется в пустую строку.

**`PDO::ATTR_STRINGIFY_FETCHES`**

Чи слід перетворювати числові значення у рядки під час вибірки. Приймає логічне значення (bool): **`true`**для включения и**`false`** для вимикання.

**`PDO::ATTR_STATEMENT_CLASS`**

Установка користувача класу оператора, похідного від PDOStatement. Потрібно `array(string classname, array(mixed constructor_args))`

**Застереження**

Не можна використовувати з постійними екземплярами PDO.

**`PDO::ATTR_TIMEOUT`**

Вказує тривалість очікування в секундах. Приймає значення як цілого числа (int).

> **Зауваження** :
> 
> Не всі драйвери підтримують цей параметр і його значення може відрізнятися від драйвера до драйвера. Наприклад, SQLite буде чекати до цього часу, перш ніж відмовитися від отримання блокування на запис, але інші драйвери можуть інтерпретувати це як інтервал очікування з'єднання або читання.

**`PDO::ATTR_AUTOCOMMIT`**

> **Зауваження**: Доступно лише для драйверів OCI, Firebird та MySQL.

Чи слід автоматично фіксувати кожен окремий оператор. Приймає логічне значення (bool): **`true`**для включения и**`false`**для отключения. По умолчанию**`true`**

**`PDO::ATTR_EMULATE_PREPARES`**

> **Зауваження**: Доступно лише для драйверів OCI, Firebird та MySQL.

Включити або вимкнути емуляцію підготовлених запитів. Деякі драйвери не підтримують підготовлені запити або мають обмежену підтримку. Якщо встановлено значення **`true`** PDO завжди буде емулювати підготовлені запити, інакше PDO намагатиметься використовувати вбудовані підготовлені запити. Якщо драйвер не зможе успішно підготувати поточний запит, PDO завжди повертатиметься до емуляції підготовленого запиту.

**`PDO::MYSQL_ATTR_USE_BUFFERED_QUERY`**

> **Зауваження**: Доступно лише для драйвера MySQL.

Визначає, чи можна використовувати буферизовані запити. Приймає логічне значення (bool): **`true`**для включения и**`false`**для отключения. По умолчанию**`true`**

**`PDO::ATTR_DEFAULT_FETCH_MODE`**

Встановлює режим вибірки за промовчанням. Опис режимів та їх використання доступний у документації [PDOStatement::fetch()](pdostatement.fetch.md)

### Список параметрів

`attribute`

Атрибут зміни.

`value`

Значение для установки параметра`attribute`може вимагати певного типу в залежності від атрибуту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [PDO::getAttribute()](pdo.getattribute.md) \- Отримує атрибут з'єднання з базою даних
-   [PDOStatement::getAttribute()](pdostatement.getattribute.md) \- Отримання значення атрибуту запиту PDOStatement
-   [PDOStatement::setAttribute()](pdostatement.setattribute.md) \- Встановлює атрибут об'єкту PDOStatement
