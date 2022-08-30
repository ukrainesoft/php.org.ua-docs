Опції PHP/інформаційні функції

-   [« Обумовлені константи](info.constants.md)
    
-   [assertoptions »](function.assert-options.html)
    
-   [PHP Manual](index.md)
    
-   [Опции/информация PHP](book.info.md)
    
-   Опції PHP/інформаційні функції
    

# Опції PHP/інформаційні функції

## Зміст

-   [assertoptions](function.assert-options.html) — Встановлення та отримання налаштувань механізму перевірки тверджень
-   [assert](function.assert.md) — Перевіряє, чи є твердження false
-   [cligetprocesstitle](function.cli-get-process-title.html) — Повертає заголовок поточного процесу
-   [clisetprocesstitle](function.cli-set-process-title.html) - Встановлює заголовок процесу
-   [дл](function.dl.md) — Завантажує модуль PHP під час виконання
-   [extensionloaded](function.extension-loaded.html) — Визначає, чи завантажено модуль
-   [гкcollectcycles](function.gc-collect-cycles.html) - Примусовий запуск збирача сміття
-   [гкdisable](function.gc-disable.html) — Вимикає збирач циклічних посилань
-   [гкenable](function.gc-enable.html) — Включає збирач циклічних посилань
-   [гкenabled](function.gc-enabled.html) — Повертає поточний стан збирача циклічних посилань
-   [гкmemcaches](function.gc-mem-caches.html) — Звільняє пам'ять, яку використовує менеджер пам'яті Zend Engine
-   [гкstatus](function.gc-status.html) — Повертає інформацію про поточний статус збирача сміття
-   [getcfgvar](function.get-cfg-var.html) — Витягує значення налаштування конфігурації PHP
-   [getcurrentuser](function.get-current-user.html) — Отримує ім'я власника поточного скрипту PHP
-   [getdefinedconstants](function.get-defined-constants.html) — Повертає асоціативний масив із іменами всіх констант та їх значень
-   [getextensionfuncs](function.get-extension-funcs.html) - Повертає масив імен функцій модуля
-   [getincludepath](function.get-include-path.html) — Отримання поточного значення конфігураційної установки includepath
-   [getincludedfiles](function.get-included-files.html) — Повертає масив імен увімкнених у скрипт файлів
-   [getloadedextensions](function.get-loaded-extensions.html) — Повертає масив імен усіх скомпілованих та завантажених модулів
-   [getmagicquotesgpc](function.get-magic-quotes-gpc.html) — Отримання поточного значення конфігурації конфігурації magicquotesgpc
-   [getmagicquotesruntime](function.get-magic-quotes-runtime.html) — Отримання поточного значення конфігурації конфігурації magicquotesruntime
-   [getrequiredfiles](function.get-required-files.html) - Псевдонім getincludedfiles
-   [getresources](function.get-resources.html) — Повертає активні ресурси
-   [getenv](function.getenv.md) — Отримання значення змінної оточення
-   [getlastmod](function.getlastmod.md) — Отримує час останньої модифікації сторінки
-   [getmygid](function.getmygid.md) - Отримати GID власника скрипта PHP
-   [getmyinode](function.getmyinode.md) — Отримує значення inode поточного скрипту
-   [getmypid](function.getmypid.md) - Отримання ID процесу PHP
-   [getmyuid](function.getmyuid.md) — Отримання UID власника скрипта PHP
-   [getopt](function.getopt.md) — Отримує параметри зі списку аргументів командного рядка
-   [getrusage](function.getrusage.md) — Отримує інформацію про використання поточного ресурсу
-   [inialter](function.ini-alter.html) - Псевдонім iniset
-   [inigetall](function.ini-get-all.html) — Отримує всі налаштування конфігурації
-   [iniget](function.ini-get.html) — Отримує значення налаштування конфігурації
-   [inirestore](function.ini-restore.html) — Відновлює налаштування конфігурації.
-   [iniset](function.ini-set.html) — Встановлює налаштування конфігурації.
-   [memorygetpeakusage](function.memory-get-peak-usage.html) — Повертає пікове значення об'єму пам'яті, виділене PHP
-   [memorygetusage](function.memory-get-usage.html) — Повертає кількість пам'яті, виділену для PHP
-   [phpiniloadedfile](function.php-ini-loaded-file.html) — Отримати шлях до завантаженого файлу php.ini
-   [phpiniscannedfiles](function.php-ini-scanned-files.html) — Повертає список .ini-файлів, знайдених у додатковій ini-директорії
-   [phpsapiname](function.php-sapi-name.html) — Повертає тип інтерфейсу між веб-сервером та PHP
-   [phpuname](function.php-uname.html) — Повертає інформацію про операційну систему, на якій запущено PHP
-   [phpcredits](function.phpcredits.md) - Виводить список розробників PHP
-   [phpinfo](function.phpinfo.md) — Виводить інформацію про поточну конфігурацію PHP
-   [phpversion](function.phpversion.md) — Отримує поточну версію PHP
-   [putenv](function.putenv.md) — Встановлює значення змінного середовища
-   [restoreincludepath](function.restore-include-path.html) — Відновлює початкове значення конфігураційної установки includepath
-   [setincludepath](function.set-include-path.html) — Встановлює значення конфігураційної установки includepath
-   [settimelimit](function.set-time-limit.html) — Обмеження часу виконання скрипту
-   [sysgettempdir](function.sys-get-temp-dir.html) — Повертає шлях до директорії тимчасових файлів
-   [versioncompare](function.version-compare.html) - Порівнює два "стандартизовані" рядки з номером версії PHP
-   [zendthreadід](function.zend-thread-id.html) - Повертає унікальний ідентифікатор поточного потоку виконання
-   [zendversion](function.zend-version.html) - Отримує версію двигуна Zend