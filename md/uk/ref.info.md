---
navigation:
  - info.constants.md: « Зумовлені константи
  - function.assert-options.md: assert\_options »
  - index.md: PHP Manual
  - book.info.md: Опції/інформація PHP
title: Опції PHP/інформаційні функції
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Опції PHP/інформаційні функції

## Зміст

-   [assert\_options](function.assert-options.md)— Встановлення та отримання налаштувань механізму перевірки тверджень
-   [assert](function.assert.md) \- Перевіряє затвердження
-   [cli\_get\_process\_title](function.cli-get-process-title.md)— Повертає заголовок поточного процесу
-   [cli\_set\_process\_title](function.cli-set-process-title.md) \- Встановлює заголовок процесу
-   [dl](function.dl.md)— Завантажує модуль PHP під час виконання
-   [extension\_loaded](function.extension-loaded.md)— Визначає, чи завантажено модуль
-   [gc\_collect\_cycles](function.gc-collect-cycles.md) \- Примусовий запуск збирача сміття
-   [gc\_disable](function.gc-disable.md)— Вимикає збирач циклічних посилань
-   [gc\_enable](function.gc-enable.md)— Включає збирач циклічних посилань
-   [gc\_enabled](function.gc-enabled.md)— Повертає поточний стан збирача циклічних посилань
-   [gc\_mem\_caches](function.gc-mem-caches.md)— Звільняє пам'ять, яку використовує менеджер пам'яті Zend Engine
-   [gc\_status](function.gc-status.md)— Повертає інформацію про поточний статус збирача сміття
-   [get\_cfg\_var](function.get-cfg-var.md)— Витягує значення конфігурації PHP
-   [get\_current\_user](function.get-current-user.md)— Отримує ім'я власника поточного скрипту PHP
-   [get\_defined\_constants](function.get-defined-constants.md)— Повертає асоціативний масив із іменами всіх констант та їх значень
-   [get\_extension\_funcs](function.get-extension-funcs.md) \- Повертає масив імен функцій модуля
-   [get\_include\_path](function.get-include-path.md)— Отримання поточного значення конфігураційної установки include\_path
-   [get\_included\_files](function.get-included-files.md)— Повертає масив імен увімкнених у скрипт файлів
-   [get\_loaded\_extensions](function.get-loaded-extensions.md)— Повертає масив імен усіх скомпілованих та завантажених модулів
-   [get\_magic\_quotes\_gpc](function.get-magic-quotes-gpc.md)— Отримання поточного значення конфігурації конфігурації magic\_quotes\_gpc
-   [get\_magic\_quotes\_runtime](function.get-magic-quotes-runtime.md)— Отримання поточного значення конфігурації конфігурації magic\_quotes\_runtime
-   [get\_required\_files](function.get-required-files.md) \- Псевдонім get\_included\_files
-   [get\_resources](function.get-resources.md)— Повертає активні ресурси
-   [getenv](function.getenv.md)— Отримує значення однієї чи всіх змінних оточення
-   [getlastmod](function.getlastmod.md)— Отримує час останньої модифікації сторінки
-   [getmygid](function.getmygid.md) \- Отримати GID власника скрипта PHP
-   [getmyinode](function.getmyinode.md)— Отримує значення inode поточного скрипту
-   [getmypid](function.getmypid.md) \- Отримання ID процесу PHP
-   [getmyuid](function.getmyuid.md)— Отримання UID власника скрипта PHP
-   [getopt](function.getopt.md)— Отримує параметри зі списку аргументів командного рядка
-   [getrusage](function.getrusage.md)— Отримує інформацію про використання поточного ресурсу
-   [ini\_alter](function.ini-alter.md) \- Псевдонім ini\_set
-   [ini\_get\_all](function.ini-get-all.md)— Отримує всі налаштування конфігурації
-   [ini\_get](function.ini-get.md)— Отримує значення налаштування конфігурації
-   [ini\_parse\_quantity](function.ini-parse-quantity.md)— Get interpreted size from ini shorthand syntax
-   [ini\_restore](function.ini-restore.md)— Відновлює налаштування конфігурації.
-   [ini\_set](function.ini-set.md)— Встановлює налаштування конфігурації.
-   [memory\_get\_peak\_usage](function.memory-get-peak-usage.md)— Повертає пікове значення об'єму пам'яті, виділеної PHP
-   [memory\_get\_usage](function.memory-get-usage.md)— Повертає кількість пам'яті, виділеної для PHP
-   [memory\_reset\_peak\_usage](function.memory-reset-peak-usage.md)— Скидає пікове значення обсягу пам'яті, виділеної PHP
-   [php\_ini\_loaded\_file](function.php-ini-loaded-file.md)— Отримати шлях до завантаженого файлу php.ini
-   [php\_ini\_scanned\_files](function.php-ini-scanned-files.md)— Повертає список .ini-файлів, знайдених у додатковій ini-директорії
-   [php\_sapi\_name](function.php-sapi-name.md)— Повертає тип інтерфейсу між веб-сервером та PHP
-   [php\_uname](function.php-uname.md)— Повертає інформацію про операційну систему, на якій запущено PHP
-   [phpcredits](function.phpcredits.md) \- Виводить список розробників PHP
-   [phpinfo](function.phpinfo.md)— Виводить інформацію про поточну конфігурацію PHP
-   [phpversion](function.phpversion.md)— Отримує поточну версію PHP
-   [putenv](function.putenv.md)— Встановлює значення змінного середовища
-   [restore\_include\_path](function.restore-include-path.md)— Відновлює початкове значення конфігураційної установки include\_path
-   [set\_include\_path](function.set-include-path.md)— Встановлює значення конфігураційної установки include\_path
-   [set\_time\_limit](function.set-time-limit.md)— Обмеження часу виконання скрипту
-   [sys\_get\_temp\_dir](function.sys-get-temp-dir.md)— Повертає шлях до директорії тимчасових файлів
-   [version\_compare](function.version-compare.md)— Порівнює два «стандартизовані» рядки з номером версії PHP
-   [zend\_thread\_id](function.zend-thread-id.md) \- Повертає унікальний ідентифікатор поточного потоку виконання
-   [zend\_version](function.zend-version.md) \- Отримує версію двигуна Zend
