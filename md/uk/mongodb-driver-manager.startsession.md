---
navigation:
  - mongodb-driver-manager.selectserver.md: '« MongoDB\\Driver\\Manager::selectServer'
  - class.mongodb-driver-command.md: MongoDB\\Driver\\Command »
  - index.md: PHP Manual
  - class.mongodb-driver-manager.md: MongoDB\\Driver\\Manager
title: 'MongoDB\\Driver\\Manager::startSession'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Manager::startSession

(mongodb >=1.4.0)

MongoDB\\Driver\\Manager::startSession — Запуск нового клієнтського сеансу для використання з цим клієнтом

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::startSession(?array $options = null): MongoDB\Driver\Session
```

Створює [MongoDB\\Driver\\Session](class.mongodb-driver-session.md) для вказаних параметрів. Сеанс потім може бути вказаний під час виконання команд, запитів та операцій запису.

> **Зауваження** [MongoDB\\Driver\\Session](class.mongodb-driver-session.md) може використовуватися тільки з [MongoDB\\Driver\\Manager](class.mongodb-driver-manager.md), З якого він був створений.

### Список параметрів

`options`

**options**

| Опция | Тип | Опис | По умолчанию |
| --- | --- | --- | --- |
| causalConsistency | bool |  |  |
| Налаштовує причинну узгодженість у сеансі. Якщо **`true`**, кожна операція у сеансі буде причинно упорядкована після попередньої операції читання чи запису. Встановіть на **`false`**, щоб вимкнути причинну узгодженість. |  |  |  |

Смотрите[» Причинну узгодженість](https://www.mongodb.com/docs/manual/core/read-isolation-consistency-recency/#causal-consistency) у посібнику MongoDB для отримання додаткової інформації.

**`true`**| | defaultTransactionOptions | array |

Параметри за замовчуванням для застосування до нових транзакцій. Ці параметри використовуються, якщо вони не перевизначаються, коли транзакція запускається з різним значенням кожного параметра.

**options**

| Опция | Тип | Опис |
| --- | --- | --- |
| maxCommitTimeMS | integer |  |
| Максимальний період часу в мілісекундах, протягом якого може виконуватись одна команда `commitTransaction` |  |  |

Якщо зазначено, `maxCommitTimeMS` має бути 32-розрядним цілим числом зі знаком, великим або рівним нулю.

| | readConcern |[MongoDB\\Driver\\ReadConcern](class.mongodb-driver-readconcern.md)

Гарантія для застосування до операції.

Ця опція доступна в MongoDB 3.2+ і призведе до виключення під час виконання, якщо вказана для старої версії сервера.

| | readPreference |[MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.md)

Перевага читання, що використовується для вибору сервера для виконання операції.

| | writeConcern |[MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.md)

Гарантія запису для застосування до операції.

Ця опція доступна у MongoDB 4.0+.

`[]`| | snapshot | bool |

Опція настроює читання миттєвих знімків у сесії. Якщо **`true`**, временная метка будет получена из первой поддерживаемой операции чтения в сессии (т.е`find` `aggregate`или unsharded`distinct`). Наступні операції читання в рамках сесії будуть використовувати рівень гарантії читання `"snapshot"` для читання даних, підтверджених більшістю, із цієї тимчасової мітки. Встановіть значення **`false`** для вимикання моментальних знімків.

Для читання моментальних знімків потрібно MongoDB 5.0+, і їх не можна використовувати з причинно-узгодженим зв'язком, транзакціями чи операціями запису. Якщо `"snapshot"`равен\*\*`true`\*\* `"causalConsistency"` за замовчуванням буде **`false`**

Смотрите[» гарантію читання "snapshot"](https://www.mongodb.com/docs/manual/reference/read-concern-snapshot/#read-concern-and-atclustertime) у посібнику MongoDB для отримання додаткової інформації.

**`false`**

### Значення, що повертаються

Повертає [MongoDB\\Driver\\Session](class.mongodb-driver-session.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Викидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо опції`"causalConsistency"`и`"snapshot"`рівні\*\*`true`\*\*
-   Викидає виняток [MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.md)якщо сеанс не може бути створений (наприклад, libmongoc не підтримує шифрування).

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.11.0 |  |
| Добавлен параметр`"snapshot"` |  |

| | PECL mongodb 1.6.0 |

Параметр`"maxCommitTimeMS"`добавлен в`"defaultTransactionOptions"`

| | PECL mongodb 1.5.0 |

Добавлена опция`"defaultTransactionOptions"`

### Дивіться також

-   [MongoDB\\Driver\\Session](class.mongodb-driver-session.md)
-   [» Причинна узгодженість](https://www.mongodb.com/docs/manual/core/read-isolation-consistency-recency/#causal-consistency)у посібнику MongoDB
