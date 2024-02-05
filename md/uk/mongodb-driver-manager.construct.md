---
navigation:
  - mongodb-driver-manager.addsubscriber.md: '« MongoDB\\Driver\\Manager::addSubscriber'
  - mongodb-driver-manager.createclientencryption.md: 'MongoDB\\Driver\\Manager::createClientEncryption »'
  - index.md: PHP Manual
  - class.mongodb-driver-manager.md: MongoDB\\Driver\\Manager
title: 'MongoDB\\Driver\\Manager::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Manager::\_\_construct

(mongodb >=1.0.0)

MongoDB\\Driver\\Manager::\_\_construct — Створює новий Manager MongoDB

### Опис

```methodsynopsis
final public MongoDB\Driver\Manager::__construct(?string $uri = null, ?array $uriOptions = null, ?array $driverOptions = null)
```

Створює новий об'єкт [MongoDB\\Driver\\Manager](class.mongodb-driver-manager.md) із переданими параметрами.

> **Зауваження**: В[» специфікації з виявлення та моніторингу сервера](https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst#single-threaded-client-construction), цей конструктор не виконує введення-виведення. З'єднання ініціалізуватимуться на вимогу, коли виконується перша операція.

> **Зауваження**: Під час передачі будь-яких URI-опцій, пов'язаних з SSL або TLS, через рядок підключення або параметр `uriOptions`драйвер неявно включає TLS при з'єднаннях. Щоб запобігти цьому, або явно вимкніть опцію `tls`, або не передавайте TLS-опцій.

> **Зауваження**: На Unix, драйвер MongoDB чутливий до сценаріїв, які використовують системний виклик fork() без наступного exec(). Користувачам рекомендується не перевикористовувати екземпляр [MongoDB\\Driver\\Manager](class.mongodb-driver-manager.md)в дочернем процессе. child process.

### Список параметрів

`uri`

URI-адрес подключения[» mongodb://](https://www.mongodb.com/docs/manual/reference/connection-string/) :

mongodb://\[username:password@\]host1\[:port1\]\[,host2\[:port2\],...\[,hostN\[:portN\]\]\]\[ \[defaultAuthDb\]\[?options\]\]

Докладніше про параметри, що підтримуються URI, дивіться розділ [» Параметри рядка підключення](https://www.mongodb.com/docs/manual/reference/connection-string/#connections-connection-options)в руководстве MongoDB[» Параметри пулу підключення](https://www.mongodb.com/docs/manual/reference/connection-string/#connection-pool-options) не підтримуються, тому що PHP-драйвер не реалізує пули підключень.

`uri` — це URL, тому будь-які спеціальні символи в його компонентах мають бути закодовані відповідно [» RFC 3986](http://www.faqs.org/rfcs/rfc3986). Це особливо актуально для імені користувача та пароля, які часто можуть містити спеціальні символи, такі як `@` `:` , или`%`. При підключенні через доменний сокет Unix шлях сокету може містити спеціальні символи, наприклад сліші, які необхідно закодувати. Функція [rawurlencode()](function.rawurlencode.md) може використовуватися для кодування складових частин URI-адреси.

Компонент`defaultAuthDb` може використовуватися для визначення імені бази даних, пов'язаної з обліковими даними користувача; однак параметр URI `authSource` матиме пріоритет, якщо він зазначений. Якщо не `defaultAuthDb`, ни`authSource` не вказано, база даних `admin`будет использоваться по умолчанию. Компонент`defaultAuthDb` немає сенсу за відсутності облікових даних користувача.

`uriOptions`

Додаткові [» параметри рядка підключення](https://www.mongodb.com/docs/manual/reference/connection-string/#connections-connection-options), які будуть перезаписувати будь-які параметри з тим самим ім'ям у параметрі `uri`

**uriOptions**

| Название опции | Тип | Опис |
| --- | --- | --- |
| appname | string |  |
| У MongoDB 3.4+ з'явилася можливість додавати анотації до з'єднань з метаданими, що надаються клієнтом, що підключається. Ці метадані включаються до журналів логування сервера під час встановлення з'єднання, а також записуються до журналів повільних запитів, якщо увімкнено профіль бази даних. |  |  |

Ця опція може використовуватися для вказівки імені програми, яка буде включена до метаданих. Значення не може перевищувати 128 символів.

| | authMechanism | string |

Механізм автентифікації, який MongoDB використовуватиме для автентифікації з'єднання. Щоб переглянути додаткові відомості та список підтримуваних значень, див. [» Параметри аутентифікації](https://www.mongodb.com/docs/manual/reference/connection-string/#urioption.authMechanism)в руководстве MongoDB.

| | authMechanismProperties | array |

Властивості обраного механізму аутентифікації. Щоб переглянути додаткові відомості та список підтримуваних значень, див. [» Специфікація аутентифікації драйвера](https://github.com/mongodb/specifications/blob/master/source/auth/auth.rst#auth-related-options)

> **Зауваження**: Якщо не вказано у рядку URI-адреси, ця опція подається у вигляді масиву пар ключ-значення. Ключі та значення в цьому масиві мають бути рядками.

| | authSource | string |

Ім'я бази даних, пов'язане з обліковими даними користувача. За замовчуванням використовується компонент бази даних із URI-адреси з'єднання або база даних `admin`якщо обидва не вказані.

Для механізмів автентифікації, які делегують зберігання облікових даних іншим службам (наприклад, GSSAPI), значення має бути `"$external"`

| | canonicalizeHostname | bool |

Якщо **`true`**, драйвер буде перетворювати реальне ім'я хоста для IP-адреси сервера перед автентифікацією через SASL. Деякі базові шари GSSAPI вже роблять це, але ця функціональність може бути відключена в їхній конфігурації (наприклад, `krb.conf`). По умолчанию\*\*`false`\*\*

Цей параметр є застарілим псевдонімом для якості `"CANONICALIZE_HOST_NAME"`параметра URI`"authMechanismProperties"`

| | compressors | string |

Той, хто має пріоритет, список розділених комами компресорів, які клієнт хоче використовувати. Повідомлення стиснуті лише в тому випадку, якщо клієнт та сервер спільно використовують будь-які компресори, а компресор, який використовується в кожному напрямку, залежатиме від індивідуальної конфігурації сервера чи драйвера. Дивіться [» Специфікація компресії драйвера](https://github.com/mongodb/specifications/blob/master/source/compression/OP_COMPRESSED.rst#compressors) для отримання додаткової інформації.

| | connectTimeoutMS | int |

Час очікування в мілісекундах під час спроби з'єднання. За замовчуванням – 10 000 мілісекунд.

| | directConnection | bool |

Цей параметр можна використовувати для керування поведінкою виявлення набору реплік, якщо в рядку підключення вказано лише один хост. За промовчанням надання одного члена в рядку підключення призведе до встановлення прямого підключення або виявлення додаткових членів залежно від того, відсутня або відсутня опція URI `"replicaSet"`соответственно. Укажите\*\*`false`\*\*, щоб викликати виявлення (якщо `"replicaSet"` опущений) або вкажіть **`true`**, щоб форсувати пряме з'єднання (якщо `"replicaSet"` присутній).

| | gssapiServiceName | string |

Встановлює ім'я Kerberos при підключенні до керберизованих екземплярів MongoDB. Це значення має співпадати з ім'ям служби, встановленим в примірниках MongoDB (тобто з параметром сервер, [» saslServiceName](https://www.mongodb.com/docs/manual/reference/parameters/#param.saslServiceName)). По умолчанию используется`"mongodb"`

Цей параметр є застарілим псевдонімом для якості `"SERVICE_NAME"`параметра URI`"authMechanismProperties"`

| | heartbeatFrequencyMS | int |

Задає інтервал у мілісекундах між перевірками драйвера топології MongoDB, які відраховуються з кінця попередньої перевірки до початку наступної. За замовчуванням – 60 000 мілісекунд.

Согласно[» Специфікації з виявлення та моніторингу сервера](https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst#heartbeatfrequencyms), це значення не може бути менше 500 мілісекунд.

| | journal | bool |

Відповідає параметру гарантій запису `journal`. Якщо **`true`**, для запису буде потрібно підтвердження MongoDB, що операція була записана в журнал. Детальніше дивіться [MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.md)

| | loadBalanced | bool |

Вказує, чи драйвер підключається до кластера MongoDB через балансувальник навантаження. Якщо **`true`**, драйвер може підключатися тільки до одного вузла (зазначеному або рядком підключення, або пошуком SRV), параметр URI `"directConnection"` не може бути \*\*`true`\*\*и опция URI`"replicaSet"` має бути опущена. За замовчуванням **`false`**

| | localThresholdMS | int |

Розмір у мілісекундах вікна затримки для вибору серед кількох відповідних екземплярів MongoDB при вирішенні переваги читання. За замовчуванням – 15 мілісекунд.

| | maxStalenessSeconds | int |

Соответствует параметру предпочтения чтения`"maxStalenessSeconds"`. Вказує в секундах, наскільки застарілим може бути вторинний вузол у наборі реплік, перш ніж клієнт перестане використовувати його для операцій читання. За замовчуванням не встановлено максимального відставання реплікації (staleness) і клієнти не враховуватимуть відставання вторинного вузла при виборі напрямку операції читання. Докладніше про це розказано в описі класу [MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.md)

Якщо зазначено, максимальне відставання має бути 32-бітовим цілим числом, більшим або рівним **`MongoDB\Driver\ReadPreference::SMALLEST_MAX_STALENESS_SECONDS`**(т. е. 90 секунд).

| | password | string | Пароль для автентифікації користувача. Ця опція є корисною, якщо пароль містить спеціальні символи, які в іншому випадку повинні були закодовані для URI-адреси підключення. | | readConcernLevel | string | Відповідає параметру гарантій читання `level`Определяет уровень изоляции чтения. Подробнее смотрите[MongoDB\\Driver\\ReadConcern](class.mongodb-driver-readconcern.md)| | readPreference | string |

Соответствует параметру предпочтениям чтения`mode`По умолчанию —`"primary"`Подробнее смотрите[MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.md)

| | readPreferenceTags | array |

Соответствует параметру предпочтениям чтения`tagSets`. Набір тегів дозволяє настроїти операції читання для певних членів набору репліки. Детальніше дивіться [MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.md)

> **Зауваження**: Якщо у рядку URI не вказано, цей параметр подається як масив, що відповідає формату, що очікується [MongoDB\\Driver\\ReadPreference::\_\_construct()](mongodb-driver-readpreference.construct.md)

| | replicaSet | string |

Вказує ім'я набору репліки.

| | retryReads | bool |

Вказує, чи має драйвер автоматично повторювати певні операції читання, які не виконуються через тимчасові мережеві помилки або вибори набору реплік. Потрібен MongoDB 3.6+. За замовчуванням **`true`**

Смотрите[» Специфікацію з Retryable Reads](https://github.com/mongodb/specifications/blob/master/source/retryable-reads/retryable-reads.rst) для отримання додаткової інформації.

| | retryWrites | bool |

Вказує, чи повинен драйвер автоматично повторювати певні операції запису, які не виконуються через тимчасові помилки мережі або вибір набору реплік. Потрібен MongoDB 3.6+. За замовчуванням **`true`**

Смотрите[» Retryable Writes](https://www.mongodb.com/docs/manual/core/retryable-writes/) у посібнику MongoDB для отримання додаткової інформації.

| | safe | bool |

Якщо **`true`**, вказує для параметра`w` гарантії запису за замовчуванням. Якщо **`false`**, вказується Подробнее смотрите[MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.md)

Ця опція застаріла і не повинна використовуватись.

| | serverSelectionTimeoutMS | int |

Вказує як довго в мілісекунді блокувати вибір сервера перед викидом виключення. За замовчуванням – 30 000 мілісекунд.

| | serverSelectionTryOnce | bool |

Якщо **`true`**, то повідомляє драйверу сканувати розгортання MongoDB лише один раз після невдалої спроби вибору сервера, а потім або вибрати сервер або створити помилку. Коли **`false`**, драйвер блокує вибір і виконує пошук сервера до закінчення часу, вказаного у параметрі `"serverSelectionTimeoutMS"`По умолчанию -**`true`**

| | socketCheckIntervalMS | int |

Якщо не використовувався сокет останнім часом, драйвер повинен перевірити за допомогою команди `hello`, перш ніж використовувати його для будь-якої операції. За замовчуванням – 5 000 мілісекунд.

| | socketTimeoutMS | int |

Час у мілісекундах, щоб спробувати відправити або отримати в сокет до закінчення часу. За замовчуванням – 300 000 мілісекунд (тобто 5 хвилин).

| | srvMaxHosts | int |

Максимальна кількість результатів SRV для випадкового вибору при початковому заповненні посівного списку або під час опитування SRV при додаванні нових вузлів до топології. За замовчуванням (т. е. без максимума).

| | srvServiceName | string |

Ім'я служби, що використовується для пошуку SRV в початковому списку DNS seedlist виявлення та опитування SRV. За замовчуванням `"mongodb"`

| | ssl | bool |

Створює з'єднання з TLS/SSL, якщо **`true`**По умолчанию -**`false`**

Параметр является устаревшим псевдонимом для параметра URI`"tls"`

| | tls | bool |

Ініціює з'єднання з TLS/SSL, якщо **`true`**По умолчанию**`false`**

| | tlsAllowInvalidCertificates | bool |

Вказує, чи має драйвер видавати помилку, якщо сертифікат сервера TLS недійсний. За замовчуванням **`false`**

**Увага**

Вимкнення перевірки сертифіката створює вразливість.

| | tlsAllowInvalidHostnames | bool |

Вказує, чи має драйвер видавати помилку при невідповідності імені хоста сервера та імені хоста, вказаного в сертифікаті TLS. За замовчуванням **`false`**

**Увага**

Вимкнення перевірки сертифіката створює вразливість. Дозвіл неприпустимих імен хоста може призвести до атаки типу ["¦"людина посередині" (man-in-the-middle)](https://en.wikipedia.org/wiki/Man-in-the-middle_attack)

| | tlsCAFile | string |

Шлях до файлу з одним або декількома центрами сертифікації, які слід вважати довіреними під час встановлення з'єднання TLS. За умовчанням використовуватиметься сховище системних сертифікатів.

| | tlsCertificateKeyFile | string |

Шлях до файлу сертифіката клієнта або закритого ключа клієнта; якщо вони обидва необхідні, файли повинні бути об'єднані.

| | tlsCertificateKeyFilePassword | string |

Пароль для розшифрування закритого ключа клієнта (тобто параметра URI `"tlsCertificateKeyFile"`), який використовуватиметься для з'єднань TLS.

| | tlsDisableCertificateRevocationCheck | bool |

Якщо **`true`**, драйвер не намагатиметься перевірити статус відкликання сертифіката (наприклад, OCSP, CRL). За замовчуванням **`false`**

| | tlsDisableOCSPEndpointCheck | bool |

Якщо **`true`**, драйвер не намагатиметься зв'язатися з кінцевою точкою відповіді OCSP, якщо це необхідно (тобто відповідь OCSP не зшивається). За замовчуванням **`false`**

| | tlsInsecure | bool |

Послабте обмеження TLS максимально можливо. При значенні **`true`** цей параметр має той самий ефект, що і вказівка ​​значення **`true`** для обох параметрів URI `"tlsAllowInvalidCertificates"`и`"tlsAllowInvalidHostnames"`По умолчанию\*\*`false`\*\*

**Увага**

Вимкнення перевірки сертифіката створює вразливість. Дозвіл неприпустимих імен хоста може призвести до атаки типу ["¦"людина посередині" (man-in-the-middle)](https://en.wikipedia.org/wiki/Man-in-the-middle_attack)

| | username | string | Ім'я користувача для автентифікації. Ця опція є корисною, якщо ім'я користувача містить спеціальні символи, які в іншому випадку повинні бути закодовані в URL для URI-адреси підключення. | | w | int | string |

Відповідає параметру гарантій запису `w`Подробнее смотрите[MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.md)

| | wTimeoutMS | int|string |

Відповідає параметру гарантій запису `wtimeout`. Вказує термін у мілісекундах для гарантії запису. Детальніше дивіться [MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.md)

Якщо зазначено, `wTimeoutMS` має бути 32-бітовим цілим числом зі знаком, великим або рівним нулю.

| | zlibCompressionLevel | int |

Вказує рівень стиснення для використання zlib. Ця опція нічого не робить, якщо `zlib` не включений до URL опції `"compressors"`Смотрите[» Специфікація компресії драйвера](https://github.com/mongodb/specifications/blob/master/source/compression/OP_COMPRESSED.rst#zlibcompressionlevel) для отримання додаткової інформації.

`driverOptions`

**driverOptions**

| Опция | Тип | Опис |
| --- | --- | --- |
| allow\_invalid\_hostname | bool |  |
| Відключає перевірку імені хоста, якщо **`true`**По умолчанию —**`false`** |  |  |

Дозвіл неприпустимих імен хоста може призвести до атаки типу ["¦"людина посередині" (man-in-the-middle)](https://en.wikipedia.org/wiki/Man-in-the-middle_attack)

Цей параметр є застарілим псевдонімом для URI `"tlsAllowInvalidHostnames"`

| | autoEncryption | array |

Надає опції для увімкнення автоматичного шифрування на рівні поля на стороні клієнта.

> **Зауваження** :
> 
> Автоматичне шифрування — це функція тільки для Enterprise версії, яка застосовується лише до операцій над колекцією. Автоматичне шифрування не підтримується для операцій над базою даних або поданням, а операції, які не обходяться, призведуть до помилки (див. [» libmongocrypt: Список дозволів на автоматичне шифрування](https://github.com/mongodb/specifications/blob/master/source/client-side-encryption/client-side-encryption.rst#libmongocrypt-auto-encryption-allow-list)). Щоб обійти автоматичне шифрування для всіх операцій, установіть `bypassAutoEncryption`в значение\*\*`true`\*\*
> 
> Автоматичне шифрування вимагає, щоб у автентифікованого користувача був привілей [» listCollections](https://www.mongodb.com/docs/manual/reference/command/listCollections/#required-access)
> 
> Явне шифрування/дешифрування та автоматичне розшифрування – це функція Community версії. Драйвер все ще може автоматично розшифровувати, якщо у опції `bypassAutoEncryption`установлено значение\*\*`true`\*\*

Підтримуються такі опції:

**Опції для автоматичного шифрування**

| Опция | Тип | Опис |
| --- | --- | --- |
| keyVaultClient | [MongoDB\\Driver\\Manager](class.mongodb-driver-manager.md) | Менеджер маршрутизації запитів ключів даних окремий кластер MongoDB. За замовчуванням метод вибирає поточний менеджер та кластер. |
| keyVaultNamespace | string | Повний простір імен (наприклад, `"databaseName.collectionName"`), що означає колекцію, яка містить усі ключі даних, що використовуються для шифрування та дешифрування. Обов'язковий параметр. |
| kmsProviders | array |  |
| Документ, який містить конфігурацію для одного або кількох провайдерів KMS, які використовуються для шифрування ключів даних. Підтримуються провайдери `"aws"` `"azure"` `"gcp"`и`"local"`, і принаймні один з них повинен бути вказаний. |  |  |

Якщо для `"aws"` `"azure"`или`"gcp"` вказано порожній документ, драйвер спробує налаштувати провайдера, використовуючи [» Автоматичні облікові дані](https://github.com/mongodb/specifications/blob/master/source/client-side-encryption/client-side-encryption.rst#automatic-credentials)

Формат для`"aws"` виглядає наступним чином:

aws: { accessKeyId:, secretAccessKey:, sessionToken:}

Формат для`"azure"` виглядає наступним чином:

azure: { tenantId:, clientId:, clientSecret:, identityPlatformEndpoint: // За замовчуванням "login.microsoftonline.com"

}

Формат для`"gcp"` виглядає наступним чином:

gcp: { email:, privateKey:|<MongoDB\\BSON\\Binary>, endpoint: // За замовчуванням "oauth2.googleapis.com"

}

Формат для`"kmip"` виглядає наступним чином:

kmip: { endpoint:}

Формат для`"local"` виглядає наступним чином:

local: { // 96-байтовий головний ключ, який використовується для шифрування/дешифрування ключів даних key: |<MongoDB\\BSON\\Binary> }

| | tlsOptions | array |

Документ, який містить конфігурацію TLS для одного або кількох KMS провайдерів. Підтримуються провайдери `"aws"` `"azure"` `"gcp"`и`"kmip"`. Усі провайдери підтримують такі опції:

: { tlsCaFile:, tlsCertificateKeyFile:, tlsCertificateKeyFilePassword:, tlsDisableOCSPEndpointCheck:}

| | schemaMap | array|object |

Карта просторів імен колекції у локальну схему JSON. Використовується для налаштування автоматичного шифрування. Додаткову інформацію дивіться у [» Правила автоматичного шифрування](https://www.mongodb.com/docs/manual/reference/security-client-side-automatic-json-schema/) в посібнику з MongoDB. Помилкою є вказівка ​​колекції як у `schemaMap`, так і в `encryptedFieldsMap`

> **Зауваження**: Добавление`schemaMap` забезпечує більшу безпеку, ніж використання схем JSON, отриманих із сервера. Це захищає від шкідливого сервера, що рекламує помилкову схему JSON, яка може змусити клієнта надсилати незашифровані дані, які мають бути зашифровані.

> **Зауваження**: Схеми, що постачаються в `schemaMap`, використовуються лише для налаштування автоматичного шифрування на стороні клієнта. Інші правила перевірки у схемі JSON не будуть використовуватися драйвером і призведуть до помилки.

| | bypassAutoEncryption | bool | Если\*\*`true`\*\* `mongocryptd` не з'являтиметься автоматично. Використовується для вимкнення автоматичного шифрування. За замовчуванням **`false`**| | bypassQueryAnalysis | bool | Если\*\*`true`**, автоматичний аналіз вихідних команд буде вимкнено та `mongocryptd` не з'являтиметься автоматично. Це дозволяє використовувати явне шифрування для запиту індексованих полів без необхідності використання ліцензованої корпоративної бібліотеки `crypt_shared`или процесса`mongocryptd`По умолчанию установлено значение**`false`\*\*| | encryptedFieldsMap | array|object |

Карта просторів імен колекції у документі `encryptedFields`. Використовується для налаштування шифрування із можливістю запиту. Дивіться [» Шифрування полів та можливість запитів](https://www.mongodb.com/docs/manual/core/queryable-encryption/fundamentals/encrypt-and-query/) у посібнику MongoDB для отримання додаткової інформації. Помилкою є вказівка ​​колекції як у `encryptedFieldsMap`, так і в `schemaMap`

> **Зауваження**: Указание`encryptedFieldsMap` забезпечує більшу безпеку, ніж покладатися на `encryptedFields`отримані від сервера. Це захищає від зловмисного сервера, що рекламує помилкові `encryptedFields`

| | extraOptions | array |

`extraOptions` відноситься до процесу `mongocryptd`. Підтримуються такі параметри:

-   `mongocryptdURI`(string): URI для підключення до існуючого процесу`mongocryptd`По умолчанию`"mongodb://localhost:27020"`
-   `mongocryptdBypassSpawn`(bool): Якщо\*\*`true`**, запобігає створенню драйвером`mongocryptd`По умолчанию**`false`\*\*
-   `mongocryptdSpawnPath`(string): Абсолютний шлях для пошуку двійкового файлу`mongocryptd`. За промовчанням це порожній рядок, який використовує системні шляхи.
-   `mongocryptdSpawnArgs`(array): Масив рядкових аргументів для передачі в`mongocryptd`при створенні. За замовчуванням`["--idleShutdownTimeoutSecs=60"]`
-   `cryptSharedLibPath`(string): Абсолютний шлях до бібліотеки загального доступу`crypt_shared`. За промовчанням — порожній рядок і використовує системні шляхи.
-   `cryptSharedLibRequired`(bool): Якщо\*\*`true`**, вимагає, щоб драйвер завантажував`crypt_shared`По умолчанию**`false`\*\*

Смотрите[» Посібник із шифрування на стороні клієнта](https://github.com/mongodb/specifications/blob/master/source/client-side-encryption/client-side-encryption.rst#extraoptions)отримати більше інформації.

> **Зауваження**: Автоматичне шифрування – це лише корпоративна функція, яка застосовується лише до операцій над колекцією. Автоматичне шифрування не підтримується для операцій з базою даних або поданням, операції, які не вдасться обійти, призведуть до помилки. Щоб обійти автоматичне шифрування для всіх операцій, установіть `bypassAutoEncryption=true`в`autoEncryption`. Для отримання додаткової інформації про дозволені операції дивіться [» Посібник із шифрування на стороні клієнта](https://github.com/mongodb/specifications/blob/master/source/client-side-encryption/client-side-encryption.rst#libmongocrypt-auto-encryption-whitelist)

| | ca\_dir | string |

Шлях до коректно захешованого каталогу сертифікатів. За умовчанням використовуватиметься сховище системних сертифікатів.

| | ca\_file | string |

Шлях до файлу з одним або декількома центрами сертифікації, які слід вважати довіреними під час встановлення з'єднання TLS. За умовчанням використовуватиметься сховище системних сертифікатів.

Параметр является устаревшим псевдонимом для параметра URI`"tlsCAFile"`

| | context | resource |

[Параметри контексту SSL](context.ssl.md) для використання як запасний варіант, якщо не вказано опцію драйвера або еквівалентну їй опцію URI. Зверніть увагу, що драйвер не звертається до контексту за промовчанням (тобто . [stream\_context\_get\_default()](function.stream-context-get-default.md)). Підтримуються такі параметри контексту:

**Резервні параметри контексту SSL**

| Параметр драйвера | Параметр контекста (запасной вариант) |
| --- | --- |
| ca\_dir | capath |
| ca\_file | cafile |
| pem\_file | local\_cert |
| pem\_pwd | passphrase |
| weak\_cert\_validation | allow\_self\_signed |

Параметр підтримується для зворотної сумісності, але слід вважати застарілим.

| | crl\_файл | string | Шлях до файлу списку анульованих сертифікатів. | | disableClientPersistence | bool |

Якщо **`true`**, Manager буде використовувати новий libmongoc клієнт, який не буде зберігатися або використовуватися іншими об'єктами Manager. Коли цей об'єкт Manager буде звільнений, його клієнт буде знищений, а всі з'єднання будуть закриті. За замовчуванням **`false`**

> **Зауваження**: Disabling client persistence is not generally recommended.

| | driver | array |

Дозволяє користувацьким драйверам додавати свої метадані до рукостискання сервера. За замовчуванням драйвер передає своє власне ім'я, версію та платформу (тобто версію PHP) у рукостискання. Драйвери користувача можуть вказувати рядки для ключів `"name"` `"version"`и`"platform"` цього масиву, які будуть додані до відповідних полів у документі рукостискання.

> **Зауваження**: Інформація про рукостискання обмежена 512 байтами. Драйвер урізає дані рукостискання, щоб відповідати цьому 512-байтовому рядку. Рекомендовано зберігати стислість метаданих драйверам і ODM.

| | pem\_file | string |

Шлях до сертифікату у форматі PEM для автентифікації клієнта.

Цей параметр є застарілим псевдонімом для URI `"tlsCertificateKeyFile"`

| | pem\_pwd | string |

Парольна фраза до PEM-закодованому сертифікату (якщо є).

Цей параметр є застарілим псевдонімом для URI `"tlsCertificateKeyFilePassword"`

| | serverApi |[MongoDB\\Driver\\ServerApi](class.mongodb-driver-serverapi.md)

Опція використовується для оголошення версії сервера API для менеджера. Якщо не вказано, версія API не оголошується.

| | weak\_cert\_validation | bool |

Відключає перевірку сертифікат, якщо **`true`**По умолчанию —**`false`**

Цей параметр є застарілим псевдонімом для URI `"tlsAllowInvalidCertificates"`

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   При неправильному форматі`uri` викидає виняток [MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.md)

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.16.0 |  |
| Провайдер AWS KMS для шифрування на стороні клієнта тепер приймає параметр `"sessionToken"`, який можна використовувати для автентифікації з тимчасовими обліковими даними AWS. |  |

Добавлено`"tlsDisableOCSPEndpointCheck"`в поле`"tlsOptions"`поля`"autoEncryption"`опции драйвера.

Якщо для KMS-провайдерів `"azure"`или`"gcp"` вказано порожній документ, драйвер спробує налаштувати провайдера, заповнивши [» Автоматичні облікові дані](https://github.com/mongodb/specifications/blob/master/source/client-side-encryption/client-side-encryption.rst#automatic-credentials)

| | PECL mongodb 1.15.0 |

Якщо для KMS-провайдера `"aws"` вказано порожній документ, драйвер спробує налаштувати провайдера, заповнивши [» Автоматичні облікові дані](https://github.com/mongodb/specifications/blob/master/source/client-side-encryption/client-side-encryption.rst#automatic-credentials)

| | PECL mongodb 1.14.0 |

Додані опції автоматичного шифрування `"bypassQueryAnalysis"`и`"encryptedFieldsMap"`. Додаткові опції, що стосуються `crypt_shared`, тепер підтримуються в опції автоматичного шифрування `"extraOptions"`option.

| | PECL mongodb 1.13.0 |

Додані URI опції `"srvMaxHosts"`и`"srvServiceName"`

| | PECL mongodb 1.12.0 |

KMIP тепер підтримується як KMS провайдер для шифрування на стороні клієнта і може бути налаштований за допомогою поля `"kmsProviders"`параметра драйвера`"autoEncryption"`. Крім того, параметри TLS для KMS-провайдерів тепер можна налаштувати у полі `"tlsOptions"`параметра драйвера`"autoEncryption"`

| | PECL mongodb 1.11.0 |

Добавлена опция URI`"loadBalanced"`

| | PECL mongodb 1.10.0 |

Добавлена опция драйвера`"disableClientPersistence"`

Azure та GCP тепер підтримуються як постачальники KMS для шифрування на стороні клієнта і можуть бути налаштовані в полі `"kmsProviders"`параметра драйвера`"autoEncryption"`. Рядки в кодуванні Base64 тепер приймаються як альтернатива [MongoDB\\BSON\\Binary](class.mongodb-bson-binary.md)для параметров внутри`"kmsProviders"`

| | PECL mongodb 1.8.0 |

Додано опції URI `"directConnection"` `"tlsDisableCertificateRevocationCheck"`, и`"tlsDisableOCSPEndpointCheck"`

Добавлен параметр драйвера`"driver"`

| | PECL mongodb 1.7.0 |

Добавлена опция драйвера`"autoEncryption"`

Вказує будь-яку опцію SSL або TLS у параметрі `driverOptions` тепер неявно вмикає TLS, як це робиться для відповідних опцій URI.

| | PECL mongodb 1.6.0 |

Додано параметри URI `"retryReads"` `"tls"` `"tlsAllowInvalidCertificates"` `"tlsAllowInvalidHostnames"` `"tlsCAFile"` `"tlsCertificateKeyFile"` `"tlsCertificateKeyFilePassword"`, и`"tlsInsecure"`

Параметр URI`"retryWrites"`по умолчанию\*\*`true`\*\*

Передача URI-опції SSL або TLS через рядок підключення або параметр `uriOptions` тепер неявно включає TLS, за умови, якщо `ssl`или`tls` не рівні \*\*`false`\**TSL*не\* включається неявно для будь-яких опцій у параметрі `driverOptions`, як у попередніх версіях.

| | PECL mongodb 1.5.0 |

`"wtimeoutMS"` тепер завжди перевіряється та застосовується до гарантії запису. Раніше ця опція ігнорувалась, якщо `"w"` був <= 1, оскільки час очікування застосовується лише до реплікації.

| | PECL mongodb 1.4.0 |

Додано опції URI `"compressors"` `"retryWrites"`и`"zlibCompressionLevel"`

| | PECL mongodb 1.3.0 |

В аргументе`uriOptions` тепер є опції `"authMechanism"`и`"authMechanismProperties"`. Раніше ці опції підтримувалися лише у аргументі `uri`

| | PECL mongodb 1.2.0 |

Аргумент`uri`по умолчанию теперь`"mongodb://127.0.0.1/"`Порт по умолчанию не изменился -`27017`

Добавлен URI-параметр`"appname"`

Додані параметри драйвера `"allow_invalid_hostname"` `"ca_file"` `"ca_dir"` `"clr_file"` `"pem_file"` `"pem_pwd"`и`"weak_cert_validation"`

API потоків PHP більше не використовується для підключення до сокету. Параметр URI `"connectTimeoutMS"`теперь по умолчанию равен 10 секунд вместо[default\_socket\_timeout](filesystem.configuration.md#ini.default-socket-timeout) у попередніх версіях. Крім того, драйвер більше не підтримує все [параметри SSL-контексту](context.ssl.md)через параметр драйвера`"context"`

| | PECL mongodb 1.1.0 |

Аргумент`uri` є необов'язковим і за умовчанням дорівнює `"mongodb://localhost:27017/"`

### Приклади

**Приклад #1 Приклади використання **MongoDB\\Driver\\Manager::\_\_construct()****

Підключення до автономного вузла MongoDB:

```php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://example.com:27017");

?>
```

Підключення до автономного сайту MongoDB через доменний сокет Unix. Шлях сокету може містити спеціальні символи, наприклад сліші, які мають закодувати за допомогою [rawurlencode()](function.rawurlencode.md)

```php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://" . rawurlencode("/tmp/mongodb-27017.sock"));

?>
```

Підключення до набору реплік:

```php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://rs1.example.com,rs2.example.com/?replicaSet=myReplicaSet");

?>
```

Підключення до сегментованого кластера (тобто одну або кілька екземплярів mongos):

```php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://mongos1.example.com,mongos2.example.com/");

?>
```

Підключення до MongoDB з обліковими даними аутентифікації для конкретного користувача та бази даних:

```php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://myusername:mypassword@example.com/?authSource=databaseName");

?>
```

Підключення до MongoDB з обліковими даними аутентифікації для конкретного користувача та бази даних, де ім'я користувача або пароль містять спеціальні символи (наприклад, `@` `:` `%`). В следующем примере, строка с паролем`myp@ss:w%rd` була вручну екранована; однак [rawurlencode()](function.rawurlencode.md) може використовуватися для екранування URI компонентів, які можуть містити спеціальні символи.

```php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://myusername:mypassword@example.com/?authSource=databaseName");

?>
```

Підключення до MongoDB з автентифікацією X509:

```php
<?php

$manager = new MongoDB\Driver\Manager(
    "mongodb://example.com/?ssl=true&authMechanism=MONGODB-X509",
    [],
    [
        "pem_file" => "/path/to/client.pem",
    ]
);
?>
```

### Дивіться також

-   [Обробка підключення та збереження](mongodb.connection-handling.md)
-   [» Формат рядка з'єднання MongoDB](https://www.mongodb.com/docs/manual/reference/connection-string/)
