- [« Архітектура та внутрішній пристрій драйвера](mongodb.architecture.md)
- [З'єднання »](mongodb.connection-handling.md)

- [PHP Manual](index.md)
- [Архітектура та внутрішній пристрій драйвера](mongodb.architecture.md)
- Огляд архітектури

# Огляд архітектури

У цьому розділі пояснюється, як різні частини драйвера з'єднуються
разом. Від різних мов виконання, через модуль та до бібліотек PHP над
ними. Ця нова архітектура замінила старий модуль Mongo. Ми називаємо
новий модуль `mongodb`.

![Схема архітектури](images/f3bc48edf40d5e3e09a166c7fadc7efb-driver_arch.png)

У верхній частині цього стека знаходиться Бібліотека
PHP](https://github.com/mongodb/mongo-php-library), яку ми будемо
поширювати як пакет Composer. Ця бібліотека надасть API,
аналогічний тому, що користувачі очікують від старого драйвера
(наприклад, методи CRUD, об'єкти баз даних та колекцій, помічники
команд), і ми очікуємо, що він буде загальною залежністю для більшості
програм, створених із MongoDB. Ця бібліотека також буде
реалізовувати спільні
[» специфікації](https://github.com/mongodb/specifications) на користь
покращення узгодженості API з усіма
[» драйверами](https://www.mongodb.com/docs/drivers/), підтримуваними
MongoDB (і, сподіваємось, також деякими драйверами спільноти).

Під цією бібліотекою у нас є драйвер нижнього рівня. Цей модуль
буде ефективно пов'язувати PHP та наші системні бібліотеки
([» libmongoc](https://github.com/mongodb/mongo-c-driver) та
[» libbson](https://github.com/mongodb/mongo-c-driver/tree/master/src/libbson)).
Цей модуль надаватиме ідентичний загальнодоступний API для
найбільш важливою та чутливою до продуктивності функціональності:

- Управління з'єднанням
- BSON кодування та декодування
- Серіалізація документа об'єкта (для підтримки бібліотек ODM)
- Виконання команд та операцій запису
- Обробка запитів та курсорів

Роз'єднуючи внутрішні компоненти драйвера та високорівневий API в
модулі та бібліотеки PHP, відповідно, ми сподіваємося зменшити
навантаження на обслуговування та прискорити ітерацію нових функцій. Як приємний
побічний ефект, це також полегшить кому-небудь робити свій внесок у
драйвера. Крім того, ідентичний загальнодоступний API значно спростить
портування програми на середовища виконання PHP, незалежно від того,
чи використовує програму драйвер низького рівня безпосередньо або бібліотеку
PHP вищого рівня.

[» GridFS](https://www.mongodb.com/docs/manual/core/gridfs/) - відмінний
приклад того, чому ми вибрали цей напрямок. Хоча ми реалізували
GridFS у C для нашого старого драйвера mongo, насправді це досить
високорівнева специфікація. Його API - це просто абстракція для
доступу до двох колекцій: файлів (тобто метаданих) та частин (тобто
блоків даних). Аналогічно, весь синтаксичний цукор, знайдений у
старому драйвері mongo, такий як обробка завантажених файлів або
представлення файлів GridFS у вигляді потоків PHP, може бути реалізований на
чистий PHP. За умови, що у нас є ефективні методи для читання та
записи в колекції GridFS та завдяки нашим низькорівневим модулям ми
перекладатимемо цей API на PHP - безпрограшний варіант.

Раніше я згадував, що ми очікуємо, що бібліотека PHP буде спільною.
залежністю для більшості програм, але не для всіх. Деякі
користувачі можуть віддати перевагу дотримуватися API-інтерфейсу без
надмірностей, запропонованого модулями, або створити власну
високорівневу абстракцію (подібно до [» Doctrine MongoDB](https://github.com/doctrine/mongodb) для старого драйвера
mongo). Майбутні бібліотеки можуть містити PHP-бібліотеку,
призначену для адміністрування MongoDB, яка надає API
для різних команд керування користувачами та командами ops.
Наступна основна версія [» Doctrine MongoDB ODM](https://github.com/doctrine/mongodb-odm), швидше за все, також буде
розміщена безпосередньо над модулями.

Хоча ми продовжуватимемо підтримувати і підтримувати старий драйвер
mongo та його користувачів у найближчому майбутньому, ми запрошуємо всіх
використовувати драйвер наступного покоління та розглядати його для будь-яких
нових проектів у майбутньому. Ви можете знайти всі необхідні компоненти в
GitHub та JIRA:

| Проект                                                                                    | GitHub                                                                   | JIRA                                           |
| ----------------------------------------------------------------------------------------- | ------------------------------------------------------------------------ | ---------------------------------------------- |
| PHP бібліотека [»mongodb/mongo-php-library](https://github.com/mongodb/mongo-php-library) | [»PHPLIB](https://jira.mongodb.org/browse/PHPLIB)                        |                                                |
| PHP 5 та PHP 7 драйвер (phongo)                                                           | [»mongodb/mongo-php-driver](https://github.com/mongodb/mongo-php-driver) | [» PHPC](https://jira.mongodb.org/browse/PHPC) |

**Вихідний код драйвера та розташування JIRA**

Існуючий проект [»PHP](https://jira.mongodb.org/browse/PHP) в JIRA
залишиться відкритим для повідомлень про помилки у старому драйвері mongo, але
ми просимо вас використовувати у нових проектах те, що описувалося вище та
стосується наших драйверів наступного покоління.
