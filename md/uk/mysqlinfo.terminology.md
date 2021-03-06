- [« Огляд PHP драйверів MySQL](mysql.md)
- [Вибір API »](mysqlinfo.api.choosing.md)

- [PHP Manual](index.md)
- [Огляд PHP драйверів MySQL](mysql.md)
- огляд термінології

# Огляд термінології

У цьому розділі розповідається про можливості взаємодії
між PHP додатком та базою даних MySQL.

*Що таке API?*

Інтерфейс програмування програм (Application Programming Interface
або API), описує класи, методи, функції та змінні, які ваше
програма повинна використовуватися для виконання поставленого завдання. В
випадку PHP, API для доступу до баз даних доступні як модулі
PHP.

API може бути процедурним чи об'єктно-орієнтованим. У процедурному
API, для здійснення необхідних дій ви викликаєте функції, тоді як
в об'єктно-орієнтованому API ви інстанціюєте класи та викликаєте їх
методи. Кращим є використання
об'єктно-орієнтованого API, тому що подібний підхід більш сучасний
та дозволяє краще організувати код.

Якщо ви пишіть PHP програму, якій необхідно взаємодіяти з
базою даних MySQL, у вас є кілька API на вибір. В цьому
Документ розповідається про те, які API є і як вибрати найбільш
підходяще для вашої програми.

*Що таке Конектор?*

У документації MySQL термін *коннектор(connector)* відсилає до тієї частини
програмного забезпечення, яка дозволяє вашому додатку
з'єднатися з базою MySQL. MySQL надає конектори для
багатьох мов програмування, зокрема й у PHP.

Якщо ваша програма повинна взаємодіяти з базою даних, ви повинні
написати PHP-код для виконання таких завдань як з'єднання з базою
даних, виконання запитів та інших функцій. Для надання вашому
додатку необхідного API та для забезпечення взаємодії між
додатком та базою даних потрібне спеціальне програмне
забезпечення. Це ПЗ зазвичай називають конектором. І саме воно дозволяє
вашій програмі *з'єднатися(connect)* з базою даних.

*Що таке Драйвер?*

Драйвер - це спеціалізоване ПЗ, створене для взаємодії з
певним сервером бази даних. Драйвер також може використовувати
сторонні бібліотеки, такі як "MySQL Client Library" або "MySQL Native
Driver". Ці бібліотеки реалізують низькорівневий протокол взаємодії
із сервером MySQL.

Наприклад, конектор [PHP Data Objects
(PDO)](mysqli.overview.md#mysqli.overview.pdo) може використовувати
різні спеціалізовані драйвери для різних баз даних. Один з
них "PDO MySQL driver", призначений для взаємодії з MySQL.

Іноді люди використовують терміни конектор та драйвер, розуміючи під ними
одне і теж. Це неправильно і може призвести до плутанини. В
документації, що відноситься до MySQL, термін "драйвер" позначає ПЗ,
надає специфічну для конкретного сервера баз даних частину
конектора.

*Що таке модуль?*

У документації PHP ви, напевно, стикалися з терміном *модуль
(Extension)*. Код PHP складається з базового функціоналу (ядра) та
необов'язкових модулів, що доповнюють функціональність ядра. Пов'язаний з
MySQL модуль PHP, `mysqli`, реалізований з використанням інфраструктури
модулів PHP

Зазвичай, модулі надають API для програміста, щоб він міг
використовувати їхню функціональність у своїх програмах. Проте існують
модулі, що не надають жодного API.

Наприклад модуль "PDO MySQL driver" не надає жодного API для
розробника. Натомість він надає інтерфейс для вищестоящого
рівня PDO.

Терміни API та Модуль позначають різні речі, оскільки модуль може не
надавати жодного API.
