ZooKeeper

-   [« ZMQDevice::setTimerTimeout](zmqdevice.settimertimeout.html)
    
-   [Введение »](intro.zookeeper.html)
    
-   [PHP Manual](index.html)
    
-   [Другие службы](refs.remote.other.html)
    
-   ZooKeeper
    

# ZooKeeper

-   [Введение](intro.zookeeper.html)
-   [Установка и настройка](zookeeper.setup.html)
    -   [Требования](zookeeper.requirements.html)
    -   [Установка](zookeeper.installation.html)
    -   [Настройка во время выполнения](zookeeper.configuration.html)
    -   [Типы ресурсов](zookeeper.resources.html)
-   [Предопределённые константы](zookeeper.constants.html)
-   [Функции ZooKeeper](ref.zookeeper.html)
    -   [zookeeperdispatch](function.zookeeper-dispatch.html) — Викликати callback-функції для операцій, що очікують
-   [Zookeeper](class.zookeeper.html) - Клас Zookeeper
    -   [Zookeeper::addAuth](zookeeper.addauth.html) — Вказує облікові дані програми
    -   [Zookeeper::close](zookeeper.close.html) — Закриває обробник zookeeper та звільняє будь-які ресурси
    -   [Zookeeper::connect](zookeeper.connect.html) — Створює дескриптор для спілкування із zookeeper
    -   [Zookeeper::construct](zookeeper.construct.html) — Створює дескриптор для спілкування із zookeeper
    -   [Zookeeper::create](zookeeper.create.html) - Створює синхронно вузол
    -   [Zookeeper::delete](zookeeper.delete.html) — Видаляє синхронно вузол у zookeeper
    -   [Zookeeper::exists](zookeeper.exists.html) — Синхронно перевіряє наявність вузла в zookeeper
    -   [Zookeeper::get](zookeeper.get.html) — Синхронно отримує дані, пов'язані із вузлом
    -   [Zookeeper::getAcl](zookeeper.getacl.html) — Синхронно отримує ACL, пов'язаний із вузлом
    -   [Zookeeper::getChildren](zookeeper.getchildren.html) - Виводить список нащадків вузла синхронно
    -   [Zookeeper::getClientId](zookeeper.getclientid.html) — Повертає ідентифікатор сесії клієнта, дійсний лише в тому випадку, якщо підключення в даний час підключено (тобто останній стан спостерігача - ZOOCONNECTEDSTATE)
    -   [Zookeeper::getConfig](zookeeper.getconfig.html) — Отримує екземпляр ZookeeperConfig
    -   [Zookeeper::getRecvTimeout](zookeeper.getrecvtimeout.html) — Повертає час очікування для сесії, дійсний тільки якщо підключення в даний час підключено (тобто останній стан спостерігача - ZOOCONNECTEDSTATE). Це значення може змінитися після повторного підключення до сервера
    -   [Zookeeper::getState](zookeeper.getstate.html) — Отримує стан з'єднання zookeeper
    -   [Zookeeper::isRecoverable](zookeeper.isrecoverable.html) — Перевіряє, чи можна відновити поточний стан підключення ZooKeeper
    -   [Zookeeper::set](zookeeper.set.html) - Встановлює дані, пов'язані з вузлом
    -   [Zookeeper::setAcl](zookeeper.setacl.html) — Встановлює ACL, пов'язаний із вузлом синхронно
    -   [Zookeeper::setDebugLevel](zookeeper.setdebuglevel.html) — Встановлює рівень логування для бібліотеки
    -   [Zookeeper::setDeterministicConnOrder](zookeeper.setdeterministicconnorder.html) - Увімкнення/відключення рандомізації порядку кінцевих точок кворуму
    -   [Zookeeper::setLogStream](zookeeper.setlogstream.html) — Встановлює потік, який використовуватиме бібліотека для логування
    -   [Zookeeper::setWatcher](zookeeper.setwatcher.html) - Встановлює функцію спостерігача
-   [ZookeeperConfig](class.zookeeperconfig.html) - Клас ZookeeperConfig
    -   [ZookeeperConfig::add](zookeeperconfig.add.html) — Додає сервери до ансамблю
    -   [ZookeeperConfig::get](zookeeperconfig.get.html) — Синхронно отримує останню підтверджену конфігурацію кластера ZooKeeper, про яку відомо серверу, до якого підключено клієнта
    -   [ZookeeperConfig::remove](zookeeperconfig.remove.html) — Видаляє сервери з ансамблю
    -   [ZookeeperConfig::set](zookeeperconfig.set.html) — Змінює склад ансамблю ZK та ролі його учасників
-   [ZookeeperException](class.zookeeperexception.html) - Клас ZookeeperException
-   [ZookeeperAuthenticationException](class.zookeeperauthenticationexception.html) - Клас ZookeeperAuthenticationException
-   [ZookeeperConnectionException](class.zookeeperconnectionexception.html) - Клас ZookeeperConnectionException
-   [ZookeeperMarshallingException](class.zookeepermarshallingexception.html) - Клас ZookeeperMarshallingException
-   [ZookeeperNoNodeException](class.zookeepernonodeexception.html) - Клас ZookeeperNoNodeException
-   [ZookeeperOperationTimeoutException](class.zookeeperoperationtimeoutexception.html) - Клас ZookeeperOperationTimeoutException
-   [ZookeeperSessionException](class.zookeepersessionexception.html) - Клас ZookeeperSessionException