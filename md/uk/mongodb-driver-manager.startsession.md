---
navigation:
  - mongodb-driver-manager.selectserver.md: '« MongoDBDriverManager::selectServer'
  - class.mongodb-driver-command.md: MongoDBDriverCommand »
  - index.md: PHP Manual
  - class.mongodb-driver-manager.md: MongoDBDriverManager
title: 'MongoDBDriverManager::startSession'
---
# MongoDBDriverManager::startSession

(mongodb >=1.4.0)

MongoDBDriverManager::startSession — Запуск нового клієнтського сеансу для використання з цим клієнтом

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::startSession(?array $options = null): MongoDB\Driver\Session
```

Створює [MongoDBDriverSession](class.mongodb-driver-session.md) для вказаних параметрів. Сеанс потім може бути вказаний під час виконання команд, запитів та операцій запису.

> **Зауваження** [MongoDBDriverSession](class.mongodb-driver-session.md) може використовуватися тільки з [MongoDBDriverManager](class.mongodb-driver-manager.md), З якого він був створений.

### Список параметрів

`options`

**options**

| Опция | Тип | Описание | По умолчанию |
| --- | --- | --- | --- |
| causalConsistency | bool |  |  |
| Налаштовує причинну узгодженість у сеансі. Якщо **`true`**, кожна операція у сеансі буде причинно упорядкована після попередньої операції читання чи запису. Встановіть на **`false`**, щоб вимкнути причинну узгодженість. |  |  |  |

Дивіться [» Причинную согласованность](https://www.mongodb.com/docs/manual/core/read-isolation-consistency-recency/#causal-consistency) у посібнику MongoDB для отримання додаткової інформації.

**`true`** | | defaultTransactionOptions | array |

Параметри за замовчуванням для застосування до нових транзакцій. Ці параметри використовуються, якщо вони не перевизначаються, коли транзакція запускається з різним значенням кожного параметра.

**options**

| Опция | Тип | Описание |
| --- | --- | --- |
| maxCommitTimeMS | integer |  |
| Максимальний період часу в мілісекундах, протягом якого може виконуватись одна команда `commitTransaction` |  |  |

Якщо зазначено, `maxCommitTimeMS` має бути 32-розрядним цілим числом зі знаком, великим або рівним нулю.

| | readConcern | [MongoDBDriverReadConcern](class.mongodb-driver-readconcern.md)

Гарантія для застосування до операції.

Ця опція доступна в MongoDB 3.2+ і призведе до виключення під час виконання, якщо вказана для старої версії сервера.

| | readPreference | [MongoDBDriverReadPreference](class.mongodb-driver-readpreference.md)

Перевага читання, що використовується для вибору сервера для виконання операції.

| | writeConcern | [MongoDBDriverWriteConcern](class.mongodb-driver-writeconcern.md)

Гарантія запису для застосування до операції.

Ця опція доступна у MongoDB 4.0+.

`[]` | | snapshot | bool |

Опція настроює читання миттєвих знімків у сесії. Якщо **`true`**, тимчасова мітка буде отримана з першої підтримуваної операції читання у сесії (тобто . `find` `aggregate` або unsharded `distinct`). Наступні операції читання в рамках сесії будуть використовувати рівень гарантії читання `"snapshot"` для читання даних, підтверджених більшістю, із цієї тимчасової мітки. Встановіть значення **`false`** для вимикання моментальних знімків.

Для читання моментальних знімків потрібно MongoDB 5.0+, і їх не можна використовувати з причинно-узгодженим зв'язком, транзакціями чи операціями запису. Якщо `"snapshot"` дорівнює **`true`** `"causalConsistency"` за замовчуванням буде **`false`**

Дивіться [» гарантію читання "snapshot"](https://www.mongodb.com/docs/manual/reference/read-concern-snapshot/#read-concern-and-atclustertime) у посібнику MongoDB для отримання додаткової інформації.

**`false`**

### Значення, що повертаються

Повертає [MongoDBDriverSession](class.mongodb-driver-session.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Викидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md) якщо опції `"causalConsistency"` і `"snapshot"` рівні **`true`**
-   Викидає виняток [MongoDBDriverExceptionRuntimeException](class.mongodb-driver-exception-runtimeexception.md) якщо сеанс не може бути створений (наприклад, libmongoc не підтримує шифрування).

### список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.11.0 |  |
| Доданий параметр `"snapshot"` |  |

| | PECL mongodb 1.6.0

Параметр `"maxCommitTimeMS"` Доданий в `"defaultTransactionOptions"`

| | PECL mongodb 1.5.0

Додана опція `"defaultTransactionOptions"`

### Дивіться також

-   [MongoDBDriverSession](class.mongodb-driver-session.md)
-   [» Причинна узгодженість](https://www.mongodb.com/docs/manual/core/read-isolation-consistency-recency/#causal-consistency) у посібнику MongoDB
