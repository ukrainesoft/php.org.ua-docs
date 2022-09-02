---
navigation:
  - function.zookeeper-dispatch.md: « zookeeperdispatch
  - zookeeper.addauth.md: 'Zookeeper::addAuth »'
  - index.md: PHP Manual
  - book.zookeeper.md: ZooKeeper
title: Клас Zookeeper
---
# Клас Zookeeper

(PECL zookeeper >= 0.1.0)

## Вступ

Представляє сесію ZooKeeper.

## Огляд класів

```classsynopsis


    
    
     
      class Zookeeper
     

     {
    

    
    /* Методы */
    
   public
   __construct(string $host = '', callable $watcher_cb = null, int $recv_timeout = 10000)

    public
   addAuth(string $scheme, string $cert, callable $completion_cb = null): bool
public
   close(): void
public
   connect(string $host, callable $watcher_cb = null, int $recv_timeout = 10000): void
public
   create(    string $path,    string $value,    array $acls,    int $flags = null): string
public
   delete(string $path, int $version = -1): bool
public
   exists(string $path, callable $watcher_cb = null): array
public
   get(    string $path,    callable $watcher_cb = null,    array &$stat = null,    int $max_size = 0): string
public
   getAcl(string $path): array
public
   getChildren(string $path, callable $watcher_cb = null): array
public
   getClientId(): int
public
   getConfig(): ZookeeperConfig
public
   getRecvTimeout(): int
public
   getState(): int
public
   isRecoverable(): bool
public
   set(    string $path,    string $value,    int $version = -1,    array &$stat = null): bool
public
   setAcl(string $path, int $version, array $acl): bool
public
   static
   setDebugLevel(int $logLevel): bool
public
   static
   setDeterministicConnOrder(bool $yesOrNo): bool
public
   setLogStream(resource $stream): bool
public
   setWatcher(callable $watcher_cb): bool

    

    
    /* Константы */
    
     const
     int
      PERM_READ = 1;

    const
     int
      PERM_WRITE = 2;

    const
     int
      PERM_CREATE = 4;

    const
     int
      PERM_DELETE = 8;

    const
     int
      PERM_ADMIN = 16;

    const
     int
      PERM_ALL = 31;


    const
         int
          EPHEMERAL = 1;

    const
     int
      SEQUENCE = 2;


    const
     int
      LOG_LEVEL_ERROR = 1;

    const
     int
      LOG_LEVEL_WARN = 2;

    const
     int
      LOG_LEVEL_INFO = 3;

    const
     int
      LOG_LEVEL_DEBUG = 4;


    const
     int
      EXPIRED_SESSION_STATE = -112;

    const
     int
      AUTH_FAILED_STATE = -113;

    const
     int
      CONNECTING_STATE = 1;

    const
     int
      ASSOCIATING_STATE = 2;

    const
     int
      CONNECTED_STATE = 3;

    const
     int
      READONLY_STATE = 5;

    const
     int
      NOTCONNECTED_STATE = 999;


    const
      int
       CREATED_EVENT = 1;

    const
     int
      DELETED_EVENT = 2;

    const
     int
      CHANGED_EVENT = 3;

    const
     int
      CHILD_EVENT = 4;

    const
     int
      SESSION_EVENT = -1;

    const
     int
      NOTWATCHING_EVENT = -2;


    const
     int
      SYSTEMERROR = -1;

    const
     int
      RUNTIMEINCONSISTENCY = -2;

    const
     int
      DATAINCONSISTENCY = -3;

    const
     int
      CONNECTIONLOSS = -4;

    const
     int
      MARSHALLINGERROR = -5;

    const
     int
      UNIMPLEMENTED = -6;

    const
     int
      OPERATIONTIMEOUT = -7;

    const
     int
      BADARGUMENTS = -8;

    const
     int
      INVALIDSTATE = -9;

    const
     int
      NEWCONFIGNOQUORUM = -13;

    const
     int
      RECONFIGINPROGRESS = -14;


    const
     int
      OK = 0;

    const
     int
      APIERROR = -100;

    const
     int
      NONODE = -101;

    const
     int
      NOAUTH = -102;

    const
     int
      BADVERSION = -103;

    const
     int
      NOCHILDRENFOREPHEMERALS = -108;

    const
     int
      NODEEXISTS = -110;

    const
     int
      NOTEMPTY = -111;

    const
     int
      SESSIONEXPIRED = -112;

    const
     int
      INVALIDCALLBACK = -113;

    const
     int
      INVALIDACL = -114;

    const
     int
      AUTHFAILED = -115;

    const
     int
      CLOSING = -116;

    const
     int
      NOTHING = -117;

    const
     int
      SESSIONMOVED = -118;

    const
     int
      NOTREADONLY = -119;

    const
     int
      EPHEMERALONLOCALSESSION = -120;

    const
     int
      NOWATCHER = -121;

    const
     int
      RECONFIGDISABLED = -122;

    

   }
```

## Обумовлені константи

## Дозволи ZooKeeper

**`Zookeeper::PERM_READ`**

Можна читати значення вузла та список дочірніх вузлів

**`Zookeeper::PERM_WRITE`**

Можна встановлювати значення вузла

**`Zookeeper::PERM_CREATE`**

Можна створювати дочірні елементи

**`Zookeeper::PERM_DELETE`**

Можна видаляти дочірні елементи

**`Zookeeper::PERM_ADMIN`**

Можна запускати setacl()

**`Zookeeper::PERM_ALL`**

Можна використовувати всі вищезгадані прапори разом

## Прапори створення ZooKeeper

**`Zookeeper::EPHEMERAL`**

Якщо встановлено прапорець Zookeeper::EPHEMERAL, вузол буде автоматично видалено після завершення клієнтської сесії.

**`Zookeeper::SEQUENCE`**

Якщо встановлено прапорець Zookeeper::SEQUENCE, до імені шляху буде додаватися унікальний номер із монотонно зростаючої послідовності. Номер із послідовності завжди має фіксовану довжину в 10 цифр, доповнену лідуючими нулями за потребою.

## Рівень логування ZooKeeper

**`Zookeeper::LOG_LEVEL_ERROR`**

Виводити лише повідомлення про помилки

**`Zookeeper::LOG_LEVEL_WARN`**

Виводити помилки та попередження

**`Zookeeper::LOG_LEVEL_INFO`**

Виводити великі повідомлення про дії, окрім помилок та попереджень

**`Zookeeper::LOG_LEVEL_DEBUG`**

Виводити все

## Стан ZooKeeper

**`Zookeeper::EXPIRED_SESSION_STATE`**

З'єднання встановлено, але сесія закінчилася

**`Zookeeper::AUTH_FAILED_STATE`**

З'єднання встановлено, але автентифікація невдала

**`Zookeeper::CONNECTING_STATE`**

Встановлюється з'єднання

**`Zookeeper::ASSOCIATING_STATE`**

Асоціювання

**`Zookeeper::CONNECTED_STATE`**

З'єднання встановлено

**`Zookeeper::READONLY_STATE`**

TODO: допоможіть нам покращити модуль

**`Zookeeper::NOTCONNECTED_STATE`**

З'єднання не встановлено

## Типи подій ZooKeeper

**`Zookeeper::CREATED_EVENT`**

Вузол був створений

Генерується лише шляхом спостереження за неіснуючими вузлами. Ці спостерігачі задаються за допомогою Zookeeper::exists.

**`Zookeeper::DELETED_EVENT`**

Вузол був видалений

Генерується лише шляхом спостереження за вузлами. Ці спостерігачі задаються за допомогою Zookeeper::exists та Zookeeper::get.

**`Zookeeper::CHANGED_EVENT`**

Вузол був змінений

Генерується лише шляхом спостереження за вузлами. Ці спостерігачі задаються за допомогою Zookeeper::exists та Zookeeper::get.

**`Zookeeper::CHILD_EVENT`**

Відбулася зміна у списку дочірніх вузлів

Генерується лише шляхом спостереження за списком дочірніх вузлів. Ці спостерігачі задаються за допомогою Zookeeper::getChildren.

**`Zookeeper::SESSION_EVENT`**

Сесія була втрачена

Генерується, коли клієнт втратив з'єднання з сервером, або ініціював переєднання.

**`Zookeeper::NOTWATCHING_EVENT`**

Спостерігач був вилучений

Генерується сервером з різних причин, наприклад, пов'язаних з обмеженням ресурсу, і говорить про те, що подальше спостереження за вузлом неможливе.

## Системні помилки та помилки на стороні сервера ZooKeeper

**`Zookeeper::SYSTEMERROR`**

Ніколи не викидається сервером і може використовуватися лише для обмеження діапазону кодів помилок. Всі помилки більші за цю, але меншу Zookeeper::APIERROR, є системними помилками.

**`Zookeeper::RUNTIMEINCONSISTENCY`**

Виявлено неузгодженість під час виконання.

**`Zookeeper::DATAINCONSISTENCY`**

Виявлено неузгодженість даних.

**`Zookeeper::CONNECTIONLOSS`**

Втрачено з'єднання із сервером.

**`Zookeeper::MARSHALLINGERROR`**

Помилка при маршалінгу та демаршалінгу даних.

**`Zookeeper::UNIMPLEMENTED`**

Операцію не реалізовано.

**`Zookeeper::OPERATIONTIMEOUT`**

Перевищення часу очікування операції.

**`Zookeeper::BADARGUMENTS`**

Неправильний аргумент.

**`Zookeeper::INVALIDSTATE`**

Некоректний статус zhandle.

**`Zookeeper::NEWCONFIGNOQUORUM`**

Кворум нової конфігурації не підключений і синхронізований із лідером останньої підтвердженої конфігурації. Спробуйте запустити переконфігурацію після підключення та синхронізації нових серверів.

Доступно з версії ZooKeeper 3.5.0

**`Zookeeper::RECONFIGINPROGRESS`**

Запит переконфігурації під час іншого процесу переконфігурації. На даний момент не підтримується. Спробуйте повторити пізніше.

Доступно з версії ZooKeeper 3.5.0

## ZooKeeper API Errors

**`Zookeeper::OK`**

Все добре.

**`Zookeeper::APIERROR`**

Ніколи не викидається сервером і може використовуватися лише для обмеження діапазону кодів помилок. Всі помилки більші за цю, є помилками API (значення менші за це означають системні помилки).

**`Zookeeper::NONODE`**

Вузол відсутній.

**`Zookeeper::NOAUTH`**

Відсутня автентифікація.

**`Zookeeper::BADVERSION`**

Конфлікт версії.

**`Zookeeper::NOCHILDRENFOREPHEMERALS`**

Ефемерні вузли не повинні мати нащадків.

**`Zookeeper::NODEEXISTS`**

Вузол уже існує.

**`Zookeeper::NOTEMPTY`**

Вузол має нащадків.

**`Zookeeper::SESSIONEXPIRED`**

Термін дії сесії минув.

**`Zookeeper::INVALIDCALLBACK`**

Вказано неправильну функцію зворотного дзвінка.

**`Zookeeper::INVALIDACL`**

Вказано некоректний ACL.

**`Zookeeper::AUTHFAILED`**

Невдала аутентифікація клієнта.

**`Zookeeper::CLOSING`**

ZooKeeper закривається.

**`Zookeeper::NOTHING`**

(не помилка) Жодної відповіді від сервера для обробки.

**`Zookeeper::SESSIONMOVED`**

Сесію переміщено на інший сервер, таким чином операцію проігноровано.

**`Zookeeper::NOTREADONLY`**

Запит зміни статусу надіслано на сервер із режимом "тільки читання".

**`Zookeeper::EPHEMERALONLOCALSESSION`**

Спроба створити ефемерний вузол у локальній сесії.

**`Zookeeper::NOWATCHER`**

Неможливо знайти спостерігача.

**`Zookeeper::RECONFIGDISABLED`**

Спроба зробити операцію переконфігурації у випадку, якщо вона заборонена.

## Зміст

-   [Zookeeper::addAuth](zookeeper.addauth.md) — Вказує облікові дані програми
-   [Zookeeper::close](zookeeper.close.md) — Закриває обробник zookeeper та звільняє будь-які ресурси
-   [Zookeeper::connect](zookeeper.connect.md) — Створює дескриптор для спілкування із zookeeper
-   [Zookeeper::construct](zookeeper.construct.md) — Створює дескриптор для спілкування із zookeeper
-   [Zookeeper::create](zookeeper.create.md) - Створює синхронно вузол
-   [Zookeeper::delete](zookeeper.delete.md) — Видаляє синхронно вузол у zookeeper
-   [Zookeeper::exists](zookeeper.exists.md) — Синхронно перевіряє наявність вузла в zookeeper
-   [Zookeeper::get](zookeeper.get.md) — Синхронно отримує дані, пов'язані із вузлом
-   [Zookeeper::getAcl](zookeeper.getacl.md) — Синхронно отримує ACL, пов'язаний із вузлом
-   [Zookeeper::getChildren](zookeeper.getchildren.md) - Виводить список нащадків вузла синхронно
-   [Zookeeper::getClientId](zookeeper.getclientid.md) — Повертає ідентифікатор сесії клієнта, дійсний лише в тому випадку, якщо підключення в даний час підключено (тобто останній стан спостерігача - ZOOCONNECTEDSTATE)
-   [Zookeeper::getConfig](zookeeper.getconfig.md) — Отримує екземпляр ZookeeperConfig
-   [Zookeeper::getRecvTimeout](zookeeper.getrecvtimeout.md) — Повертає час очікування для сесії, дійсний тільки якщо підключення в даний час підключено (тобто останній стан спостерігача - ZOOCONNECTEDSTATE). Це значення може змінитися після повторного підключення до сервера
-   [Zookeeper::getState](zookeeper.getstate.md) — Отримує стан з'єднання zookeeper
-   [Zookeeper::isRecoverable](zookeeper.isrecoverable.md) — Перевіряє, чи можна відновити поточний стан підключення ZooKeeper
-   [Zookeeper::set](zookeeper.set.md) - Встановлює дані, пов'язані з вузлом
-   [Zookeeper::setAcl](zookeeper.setacl.md) — Встановлює ACL, пов'язаний із вузлом синхронно
-   [Zookeeper::setDebugLevel](zookeeper.setdebuglevel.md) — Встановлює рівень логування для бібліотеки
-   [Zookeeper::setDeterministicConnOrder](zookeeper.setdeterministicconnorder.md) - Увімкнення/відключення рандомізації порядку кінцевих точок кворуму
-   [Zookeeper::setLogStream](zookeeper.setlogstream.md) — Встановлює потік, який використовуватиме бібліотека для логування
-   [Zookeeper::setWatcher](zookeeper.setwatcher.md) - Встановлює функцію спостерігача
