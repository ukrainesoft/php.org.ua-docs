---
navigation:
  - wincache.installation.md: « Встановлення
  - wincache.stats.md: Скрипт статистики WinCache »
  - index.md: PHP Manual
  - wincache.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

У таблиці наведено список конфігураційних параметрів модуля WinCache:

**Конфігураційні параметри WinCache**

| Имя | По умолчанию | Минимум | Максимум | Место изменения | Список изменений |
| --- | --- | --- | --- | --- | --- |
| [wincache.fcenabled](wincache.configuration.md#ini.wincache.fcenabled) | "1" | "0" | "1" | **`INI_ALL`** | Доступно з WinCache 1.0.0 |
| [wincache.fcenabledfilter](wincache.configuration.md#ini.wincache.fcenabledfilter) | "NULL" | "NULL" | "NULL" | **`INI_SYSTEM`** | Доступно з WinCache 1.0.0 |
| [wincache.fcachesize](wincache.configuration.md#ini.wincache.fcachesize) | "24" | "5" | "255" | **`INI_SYSTEM`** | Доступно з WinCache 1.0.0 |
| [wincache.fcndetect](wincache.configuration.md#ini.wincache.fcndetect) | "1" | "0" | "1" | **`INI_SYSTEM`** | Доступно з WinCache 1.1.0 |
| [wincache.maxfilesize](wincache.configuration.md#ini.wincache.maxfilesize) | "256" | "10" | "2048" | **`INI_SYSTEM`** | Доступно з WinCache 1.0.0 |
| [wincache.ocenabled](wincache.configuration.md#ini.wincache.ocenabled) | "1" | "0" | "1" | **`INI_ALL`** | Доступно з WinCache 1.0.0. Вилучено у 2.0.0.0 |
| [wincache.ocenabledfilter](wincache.configuration.md#ini.wincache.ocenabledfilter) | "NULL" | "NULL" | "NULL" | **`INI_SYSTEM`** | Доступно з WinCache 1.0.0. Вилучено у 2.0.0.0 |
| [wincache.ocachesize](wincache.configuration.md#ini.wincache.ocachesize) | "96" | "15" | "255" | **`INI_SYSTEM`** | Доступно з WinCache 1.0.0. Вилучено у 2.0.0.0 |
| [wincache.filecount](wincache.configuration.md#ini.wincache.filecount) | "4096" | "1024" | "16384" | **`INI_SYSTEM`** | Доступно з WinCache 1.0.0 |
| [wincache.chkinterval](wincache.configuration.md#ini.wincache.chkinterval) | "30" | "0" | "300" | **`INI_SYSTEM`** | Доступно з WinCache 1.0.0 |
| [wincache.ttlmax](wincache.configuration.md#ini.wincache.ttlmax) | "1200" | "0" | "7200" | **`INI_SYSTEM`** | Доступно з WinCache 1.0.0 |
| [wincache.enablecli](wincache.configuration.md#ini.wincache.enablecli) |  |  |  | **`INI_SYSTEM`** | Доступно з WinCache 1.0.0 |
| [wincache.ignorelist](wincache.configuration.md#ini.wincache.ignorelist) | NULL | NULL | NULL | **`INI_ALL`** | Доступно з WinCache 1.0.0 |
| [wincache.namesalt](wincache.configuration.md#ini.wincache.namesalt) | NULL | NULL | NULL | **`INI_SYSTEM`** | Доступно з WinCache 1.0.0 |
| [wincache.ucenabled](wincache.configuration.md#ini.wincache.ucenabled) |  |  |  | **`INI_SYSTEM`** | Доступно з WinCache 1.1.0 |
| [wincache.ucachesize](wincache.configuration.md#ini.wincache.ucachesize) | 8 | 5 | 85 | **`INI_SYSTEM`** | Доступно з WinCache 1.1.0 |
| [wincache.scachesize](wincache.configuration.md#ini.wincache.scachesize) | 8 | 5 | 85 | **`INI_SYSTEM`** | Доступно з WinCache 1.1.0 |
| [wincache.rerouteini](wincache.configuration.md#ini.wincache.rerouteini) | NULL | NULL | NULL | **`INI_SYSTEM`** | Доступно з WinCache 1.2.0. Вилучено у 1.3.7 |
| [wincache.reroute\_enabled](wincache.configuration.md#ini.wincache.reroute_enabled) |  |  |  | **`INI_SYSTEM`** | **`INI_PERDIR`** |
| [wincache.srwlocks](wincache.configuration.md#ini.wincache.srwlocks) |  |  |  | **`INI_SYSTEM`** | Доступно з WinCache 1.3.6.3. Вилучено у 2.0.0.0 |
| [wincache.filemapdir](wincache.configuration.md#ini.wincache.filemapdir) | NULL | NULL | NULL | **`INI_SYSTEM`** | Доступно з WinCache 1.3.7.4 |

Додаткова інформація та опис режимів INI\_\* дано у розділі «[Місця встановлення параметрів конфігурації](configuration.changes.modes.md)».

Коротке пояснення конфігураційних директив.

`wincache.fcenabled`bool

Вмикає/вимикає файлове кешування.

`wincache.fcenabledfilter`string

Визначає список ідентифікаторів IIS веб-серверів, розділених комою, для яких має бути дозволено/заборонено файлове кешування. Це налаштування працює в парі з `wincache.fcenabled`: якщо `wincache.fcenabled` встановлено в 1, то для серверів, перерахованих у `wincache.fcenabledfilter` файлове кешування буде вимкнено; якщо `wincache.fcenabled` встановлено як 0, то для серверів, перерахованих у `wincache.fcenabledfilter` файлове кешування буде увімкнено.

`wincache.fcachesize`int

Визначає максимальний розмір пам'яті (мегабайт) для файлового кеша. Коли розмір всіх закешованих файлів перевищить це значення, з кеша будуть видалені застарілі файли.

`wincache.fcndetect`bool

Вмикає/вимикає функцію сповіщення про зміну файлу. Якщо функціонал оповіщення про зміни файлу підтримується, він може бути використаний для оновлення кеша опкодів та файлового кеша при отриманні відповідних оповіщень. Якщо подібний механізм не підтримується, наприклад, при використанні мережевих папок, wincache самостійно перевірятиме файли на предмет зміни через задані в налаштуванні `wincache.chkinterval` інтервали часу.

`wincache.maxfilesize`int

Визначає максимальний розмір файлу (у кілобайтах) для файлового кешу. Якщо розмір файлу перевищує задане значення, він не буде закеширован. Ця установка застосовується лише до файлового кешу.

`wincache.ocenabled`bool

**Увага**

Ця опція була *ВИДАЛЕНО* у версії 2.0.0.0

Включає/вимикає кешування опкодів

`wincache.ocenabledfilter`string

**Увага**

Ця опція була *ВИДАЛЕНО* у версії 2.0.0.0

Визначає список ідентифікаторів IIS веб-серверів, розділених комою, для яких має бути дозволено/заборонено кешування опкодів. Це налаштування працює в парі з `wincache.ocenabled`: якщо `wincache.ocenabled` встановлено в 1, то для серверів, перерахованих у `wincache.ocenabledfilter` файлове кешування буде вимкнено; якщо `wincache.ocenabled` встановлено як 0, то для серверів, перерахованих у `wincache.ocenabledfilter`файловое кеширование будет разрешено.

`wincache.ocachesize`int

**Увага**

Ця опція була *ВИДАЛЕНО* у версії 2.0.0.0

Визначає максимальний розмір пам'яті (мегабайт) для кеша опкодів. Коли розмір всіх закешованих опкодів перевищить це значення, з кеша будуть видалені застарілі з них. Зверніть увагу, що кеш опкодів повинен бути щонайменше в 3 рази більшим за файловий кеш. Якщо це не так, то розмір кешу опкодів буде автоматично збільшено.

`wincache.filecount`int

Визначає, скільки файлів буде закешовано модулем, щоб при старті був виділений відповідний шматок пам'яті. Якщо кількість файлів перевищить задане значення, WinCache здійснить переаллокацію пам'яті.

`wincache.chkinterval`int

Визначає, наскільки часто (в секундах) модуль перевірятиме файли на предмет їх зміни для оновлення кешів. Значення 0 відключає цей функціонал. Зміни файлів не будуть відображені в кеші доти, доки закешований запис не буде видалено з кеша збирачем застарілих записів, або поки не буде перероблений пул додатків IIS, або не буде викликано функцію wincache\_refresh\_if\_changed.

`wincache.ttlmax`int

Визначає максимальний час (за секунди) незатребуваності для запису в кеші. Установка в 0 відключає процес видалення застарілих записів, що призведе до того, що запис лежатиме в кеші, поки сервер IIS не буде зупинений.

`wincache.enablecli`bool

Визначає, чи дозволяється кешування під час роботи PHP із командного рядка (CLI).

`wincache.ignorelist`string

Визначає список файлів, які не потрібно кешувати. Вказуються лише імена файлів. Символ роздільника - вертикальна характеристика "|".

**Приклад #1 Приклад использования`wincache.ignorelist`**

wincache.ignorelist = "index.php|misc.php|admin.php"

`wincache.namesalt`string

Визначає рядок, який буде використовуватися при іменуванні об'єктів, що розміщуються в пам'яті, що розділяється. Це необхідно для запобігання колізій, коли кілька процесів працюють з пам'яттю, що розділяється. Довжина цього рядка не повинна перевищувати 8 символів.

`wincache.ucenabled`bool

Вмикає/вимикає кеш користувача.

`wincache.ucachesize`int

Визначає максимальний розмір пам'яті (у мегабайтах) для кешу користувача. Коли розмір всіх закешованих змінних перевищить це значення, з кеша буде видалено найзастаріліші змінні.

`wincache.scachesize`int

Визначає максимальний розмір пам'яті (мегабайт) для сесійного кешу. Коли розмір всіх закешованих даних перевищить це значення, з кеша буде видалено найзастаріліші дані.

`wincache.rerouteini`string

**Увага**

Ця опція була *ВИДАЛЕНО* у версії 1.3.7. Починаючи із 1.3.7. замість неї використовуйте `wincache.reroute_enabled`

Задає абсолютний або відносний шлях до reroute.ini, який містить список функцій PHP, реалізація яких повинна бути підмінена реалізацією з модуля WinCache. Якщо заданий відносний шлях, то він буде вирішуватися щодо розташування файлу php-cgi.exe.

`wincache.reroute_enabled`bool

Вмикає/вимикає перенаправлення деяких функцій файлового введення/виводу для роботи через файловий кеш.

`wincache.srwlocks`bool

**Увага**

Ця опція була *ВИДАЛЕНО* у версії 2.0.0.0

Вмикає/вимикає використання блокувань читання/запису, що розділяються. Вимкнення корисне при налагодженні ситуацій взаємних блокувань WinCache.

`wincache.filemapdir`string

Задає абсолютний шлях до директорії, де WinCache триматиме тимчасові файли для сегментів пам'яті, що розділяється. Ця директорія повинна розташовуватись на локальній машині і в жодному разі не на мережній файловій системі. Якщо директорія не вказана, WinCache буде використовувати Windows System Page File.
