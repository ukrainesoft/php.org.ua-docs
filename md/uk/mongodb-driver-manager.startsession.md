Запуск нового клієнтського сеансу для використання з цим клієнтом

-   [« MongoDB\\Driver\\Manager::selectServer](mongodb-driver-manager.selectserver.html)
    
-   [MongoDB\\Driver\\Command »](class.mongodb-driver-command.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Manager](class.mongodb-driver-manager.html)
    
-   Запуск нового клієнтського сеансу для використання з цим клієнтом
    

# MongoDBDriverManager::startSession

(mongodb >=1.4.0)

MongoDBDriverManager::startSession — Запуск нового клієнтського сеансу для використання з цим клієнтом

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::startSession(?array $options = null): MongoDB\Driver\Session
```

Створює [MongoDB\\Driver\\Session](class.mongodb-driver-session.html) для вказаних параметрів. Сеанс потім може бути вказаний під час виконання команд, запитів та операцій запису.

> **Зауваження** [MongoDB\\Driver\\Session](class.mongodb-driver-session.html) може використовуватися тільки з [MongoDB\\Driver\\Manager](class.mongodb-driver-manager.html), З якого він був створений.

### Список параметрів

`options`

**options**

| Опция | Тип | Описание | По умолчанию |
| --- | --- | --- | --- |
| causalConsistency | bool |  |  |
| Налаштовує причинну узгодженість у сеансі. Якщо **`true`**, кожна операція у сеансі буде причинно упорядкована після попередньої операції читання чи запису. Встановіть на **`false`**, щоб вимкнути причинну узгодженість. |  |  |  |

Дивіться [» Причинную согласованность](https://www.mongodb.com/docs/manual/core/read-isolation-consistency-recency/#causal-consistency) у посібнику MongoDB для отримання додаткової інформації.

**`true`** | | defaultTransactionOptions | array |

Параметри за замовчуванням для застосування до нових транзакцій. Ці параметри використовуються, якщо вони не перевизначаються, коли транзакція запускається з різним значенням кожного параметра.

**options**

| Опция | Тип | Описание |
| --- | --- | --- |
| maxCommitTimeMS | integer |  |
| Максимальний період часу в мілісекундах, протягом якого може виконуватись одна команда `commitTransaction` |  |  |

Якщо зазначено, `maxCommitTimeMS` має бути 32-розрядним цілим числом зі знаком, великим або рівним нулю.

| | readConcern | [MongoDB\\Driver\\ReadConcern](class.mongodb-driver-readconcern.html)

Гарантія для застосування до операції.

Ця опція доступна в MongoDB 3.2+ і призведе до виключення під час виконання, якщо вказана для старої версії сервера.

| | readPreference | [MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.html)

Перевага читання, що використовується для вибору сервера для виконання операції.

| | writeConcern | [MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.html)

Гарантія запису для застосування до операції.

Ця опція доступна у MongoDB 4.0+.

`[]` | | snapshot | bool |

Опція настроює читання миттєвих знімків у сесії. Якщо **`true`**, тимчасова мітка буде отримана з першої підтримуваної операції читання у сесії (тобто . `find` `aggregate` або unsharded `distinct`). Наступні операції читання в рамках сесії будуть використовувати рівень гарантії читання `"snapshot"` для читання даних, підтверджених більшістю, із цієї тимчасової мітки. Встановіть значення **`false`** для вимикання моментальних знімків.

Для читання моментальних знімків потрібно MongoDB 5.0+, і їх не можна використовувати з причинно-узгодженим зв'язком, транзакціями чи операціями запису. Якщо `"snapshot"` дорівнює **`true`** `"causalConsistency"` за замовчуванням буде **`false`**

Дивіться [» гарантию чтения "snapshot"](https://www.mongodb.com/docs/manual/reference/read-concern-snapshot/#read-concern-and-atclustertime) у посібнику MongoDB для отримання додаткової інформації.

**`false`**

### Значення, що повертаються

Повертає [MongoDB\\Driver\\Session](class.mongodb-driver-session.html)

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Викидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html) якщо опції `"causalConsistency"` і `"snapshot"` рівні **`true`**
-   Викидає виняток [MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.html) якщо сеанс не може бути створений (наприклад, libmongoc не підтримує шифрування).

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

-   [MongoDB\\Driver\\Session](class.mongodb-driver-session.html)
-   [» Причинная согласованность](https://www.mongodb.com/docs/manual/core/read-isolation-consistency-recency/#causal-consistency) у посібнику MongoDB