Налаштування під час виконання

-   [« Установка](wincache.installation.md)
    
-   [Скрипт статистики WinCache »](wincache.stats.md)
    
-   [PHP Manual](index.md)
    
-   [Встановлення та налаштування](wincache.setup.md)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

У таблиці наведено список конфігураційних параметрів модуля WinCache:

**Конфігураційні параметри WinCache**

| Имя                                                                                  | По умолчанию | Минимум | Максимум | Место изменения | Список изменений                                |
|--------------------------------------------------------------------------------------|--------------|---------|----------|-----------------|-------------------------------------------------|
| [wincache.fcenabled](wincache.configuration.html#ini.wincache.fcenabled)             | "1"          | "0"     | "1"      | PHPINIALL       | Доступно з WinCache 1.0.0                       |
| [wincache.fcenabledfilter](wincache.configuration.html#ini.wincache.fcenabledfilter) | "NULL"       | "NULL"  | "NULL"   | PHPINISYSTEM    | Доступно з WinCache 1.0.0                       |
| [wincache.fcachesize](wincache.configuration.html#ini.wincache.fcachesize)           | "24"         | "5"     | "255"    | PHPINISYSTEM    | Доступно з WinCache 1.0.0                       |
| [wincache.fcndetect](wincache.configuration.html#ini.wincache.fcndetect)             | "1"          | "0"     | "1"      | PHPINISYSTEM    | Доступно з WinCache 1.1.0                       |
| [wincache.maxfilesize](wincache.configuration.html#ini.wincache.maxfilesize)         | "256"        | "10"    | "2048"   | PHPINISYSTEM    | Доступно з WinCache 1.0.0                       |
| [wincache.ocenabled](wincache.configuration.html#ini.wincache.ocenabled)             | "1"          | "0"     | "1"      | PHPINIALL       | Доступно з WinCache 1.0.0. Вилучено у 2.0.0.0   |
| [wincache.ocenabledfilter](wincache.configuration.html#ini.wincache.ocenabledfilter) | "NULL"       | "NULL"  | "NULL"   | PHPINISYSTEM    | Доступно з WinCache 1.0.0. Вилучено у 2.0.0.0   |
| [wincache.ocachesize](wincache.configuration.html#ini.wincache.ocachesize)           | "96"         | "15"    | "255"    | PHPINISYSTEM    | Доступно з WinCache 1.0.0. Вилучено у 2.0.0.0   |
| [wincache.filecount](wincache.configuration.html#ini.wincache.filecount)             | "4096"       | "1024"  | "16384"  | PHPINISYSTEM    | Доступно з WinCache 1.0.0                       |
| [wincache.chkinterval](wincache.configuration.html#ini.wincache.chkinterval)         | "30"         | "0"     | "300"    | PHPINISYSTEM    | Доступно з WinCache 1.0.0                       |
| [wincache.ttlmax](wincache.configuration.html#ini.wincache.ttlmax)                   | "1200"       | "0"     | "7200"   | PHPINISYSTEM    | Доступно з WinCache 1.0.0                       |
| [wincache.enablecli](wincache.configuration.html#ini.wincache.enablecli)             |              |         |          | PHPINISYSTEM    | Доступно з WinCache 1.0.0                       |
| [wincache.ignorelist](wincache.configuration.html#ini.wincache.ignorelist)           | NULL         | NULL    | NULL     | PHPINIALL       | Доступно з WinCache 1.0.0                       |
| [wincache.namesalt](wincache.configuration.html#ini.wincache.namesalt)               | NULL         | NULL    | NULL     | PHPINISYSTEM    | Доступно з WinCache 1.0.0                       |
| [wincache.ucenabled](wincache.configuration.html#ini.wincache.ucenabled)             |              |         |          | PHPINISYSTEM    | Доступно з WinCache 1.1.0                       |
| [wincache.ucachesize](wincache.configuration.html#ini.wincache.ucachesize)           |              |         |          | PHPINISYSTEM    | Доступно з WinCache 1.1.0                       |
| [wincache.scachesize](wincache.configuration.html#ini.wincache.scachesize)           |              |         |          | PHPINISYSTEM    | Доступно з WinCache 1.1.0                       |
| [wincache.rerouteini](wincache.configuration.html#ini.wincache.rerouteini)           | NULL         | NULL    | NULL     | PHPINISYSTEM    | Доступно з WinCache 1.2.0. Вилучено у 1.3.7     |
| [wincache.rerouteenabled](wincache.configuration.html#ini.wincache.reroute_enabled)  |              |         |          | PHPINISYSTEM    | PHPINIPERDIR                                    |
| [wincache.srwlocks](wincache.configuration.html#ini.wincache.srwlocks)               |              |         |          | PHPINISYSTEM    | Доступно з WinCache 1.3.6.3. Вилучено у 2.0.0.0 |
| [wincache.filemapdir](wincache.configuration.html#ini.wincache.filemapdir)           | NULL         | NULL    | NULL     | PHPINISYSTEM    | Доступно з WinCache 1.3.7.4                     |

Для детального опису констант PHPINI, зверніться до розділу [Де можуть бути встановлені параметри конфігурації](configuration.changes.modes.md)

Коротке пояснення конфігураційних директив.

`wincache.fcenabled` bool

Вмикає/вимикає файлове кешування.

`wincache.fcenabledfilter` string

Визначає список ідентифікаторів IIS веб-серверів, розділених комою, для яких має бути дозволено/заборонено файлове кешування. Це налаштування працює в парі з `wincache.fcenabled`: якщо `wincache.fcenabled` встановлено в 1, то для серверів, перерахованих у `wincache.fcenabledfilter` файлове кешування буде вимкнено; якщо `wincache.fcenabled` встановлено як 0, то для серверів, перерахованих у `wincache.fcenabledfilter` файлове кешування буде увімкнено.

`wincache.fcachesize` int

Визначає максимальний розмір пам'яті (мегабайт) для файлового кеша. Коли розмір всіх закешованих файлів перевищить це значення, з кеша будуть видалені застарілі файли.

`wincache.fcndetect` bool

Вмикає/вимикає функцію сповіщення про зміну файлу. Якщо функціонал оповіщення про зміни файлу підтримується, він може бути використаний для оновлення кеша опкодів та файлового кеша при отриманні відповідних оповіщень. Якщо подібний механізм не підтримується, наприклад, при використанні мережевих папок, wincache самостійно перевірятиме файли на предмет зміни через задані в налаштуванні `wincache.chkinterval` інтервали часу.

`wincache.maxfilesize` int

Визначає максимальний розмір файлу (у кілобайтах) для файлового кешу. Якщо розмір файлу перевищує задане значення, він не буде закеширован. Ця установка застосовується лише до файлового кешу.

`wincache.ocenabled` bool

**Увага**

Ця опція була *ВИДАЛЕНО* у версії 2.0.0.0

Включає/вимикає кешування опкодів

`wincache.ocenabledfilter` string

**Увага**

Ця опція була *ВИДАЛЕНО* у версії 2.0.0.0

Визначає список ідентифікаторів IIS веб-серверів, розділених комою, для яких має бути дозволено/заборонено кешування опкодів. Це налаштування працює в парі з `wincache.ocenabled`: якщо `wincache.ocenabled` встановлено в 1, то для серверів, перерахованих у `wincache.ocenabledfilter` файлове кешування буде вимкнено; якщо `wincache.ocenabled` встановлено як 0, то для серверів, перерахованих у `wincache.ocenabledfilter` файлове кешування буде дозволено.

`wincache.ocachesize` int

**Увага**

Ця опція була *ВИДАЛЕНО* у версії 2.0.0.0

Визначає максимальний розмір пам'яті (мегабайт) для кеша опкодів. Коли розмір всіх закешованих опкодів перевищить це значення, з кеша будуть видалені застарілі з них. Зверніть увагу, що кеш опкодів повинен бути щонайменше в 3 рази більшим за файловий кеш. Якщо це не так, то розмір кешу опкодів буде автоматично збільшено.

`wincache.filecount` int

Визначає, скільки файлів буде закешовано модулем, щоб при старті був виділений відповідний шматок пам'яті. Якщо кількість файлів перевищить задане значення, WinCache здійснить переаллокацію пам'яті.

`wincache.chkinterval` int

Визначає, наскільки часто (в секундах) модуль перевірятиме файли на предмет їх зміни для оновлення кешів. Значення 0 відключає цей функціонал. Зміни файлів не будуть відображені в кеші доти, доки закешований запис не буде видалено з кеша збирачем застарілих записів, або поки не буде перероблений пул додатків IIS, або не буде викликано функцію wincacherefreshіфchanged.

`wincache.ttlmax` int

Визначає максимальний час (за секунди) незатребуваності для запису в кеші. Установка в 0 відключає процес видалення застарілих записів, що призведе до того, що запис лежатиме в кеші, поки сервер IIS не буде зупинений.

`wincache.enablecli` bool

Визначає, чи дозволяється кешування під час роботи PHP із командного рядка (CLI).

`wincache.ignorelist` string

Визначає список файлів, які не потрібно кешувати. Вказуються лише імена файлів. Символ роздільника - вертикальна характеристика "|".

**Приклад #1 Приклад використання `wincache.ignorelist`**

wincache.ignorelist = "index.php|misc.php|admin.php"

`wincache.namesalt` string

Визначає рядок, який буде використовуватися при іменуванні об'єктів, що розміщуються в пам'яті, що розділяється. Це необхідно для запобігання колізій, коли кілька процесів працюють з пам'яттю, що розділяється. Довжина цього рядка не повинна перевищувати 8 символів.

`wincache.ucenabled` bool

Вмикає/вимикає кеш користувача.

`wincache.ucachesize` int

Визначає максимальний розмір пам'яті (у мегабайтах) для кешу користувача. Коли розмір всіх закешованих змінних перевищить це значення, з кеша буде видалено найзастаріліші змінні.

`wincache.scachesize` int

Визначає максимальний розмір пам'яті (мегабайт) для сесійного кешу. Коли розмір всіх закешованих даних перевищить це значення, з кеша буде видалено найзастаріліші дані.

`wincache.rerouteini` string

**Увага**

Ця опція була *ВИДАЛЕНО* у версії 1.3.7. Починаючи із 1.3.7. замість неї використовуйте `wincache.reroute_enabled`

Задає абсолютний або відносний шлях до reroute.ini, який містить список функцій PHP, реалізація яких повинна бути підмінена реалізацією з модуля WinCache. Якщо заданий відносний шлях, то він буде вирішуватися щодо розташування файлу php-cgi.exe.

`wincache.reroute_enabled` bool

Вмикає/вимикає перенаправлення деяких функцій файлового введення/виводу для роботи через файловий кеш.

`wincache.srwlocks` bool

**Увага**

Ця опція була *ВИДАЛЕНО* у версії 2.0.0.0

Вмикає/вимикає використання блокувань читання/запису, що розділяються. Вимкнення корисне при налагодженні ситуацій взаємних блокувань WinCache.

`wincache.filemapdir` string

Задає абсолютний шлях до директорії, де WinCache триматиме тимчасові файли для сегментів пам'яті, що розділяється. Ця директорія повинна розташовуватись на локальній машині і в жодному разі не на мережній файловій системі. Якщо директорія не вказана, WinCache буде використовувати Windows System Page File.