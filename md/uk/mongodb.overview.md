---
navigation:
  - mongodb.architecture.md: « Архітектура та внутрішній пристрій драйвера
  - mongodb.connection-handling.md: З'єднання »
  - index.md: PHP Manual
  - mongodb.architecture.md: Архітектура та внутрішній пристрій драйвера
title: Огляд архітектури
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Огляд архітектури

У цьому розділі пояснюється, як різні частини PHP-драйвера поєднуються один з одним, від базових системних бібліотек, через PHP-модулі до PHP-бібліотек на самому верху.

![Схема архітектури PHP-драйвера.
Найнижчий рівень драйвера - це системні модулі: libmongoc, libbson та libmongocrypt.
Середній рівень – це PHP-модуль MongoDB, написаний мовою Сі.
Верхній рівень - це користувальницьке оточення PHP,
PHP-модуль MongoDB та високорівневі пакети: фреймворки та програми.](images/f3bc48edf40d5e3e09a166c7fadc7efb-driver_arch.svg)

Наверху стека расположена[» бібліотека PHP](https://github.com/mongodb/mongo-php-library), яка поширюється у вигляді [» пакета Composer](https://packagist.org/packages/mongodb/mongodb). Ця бібліотека надасть API, узгоджений з іншими [» драйверами](https://www.mongodb.com/docs/drivers/) MongoDB, і реалізує міждрайверні [» специфікації](https://github.com/mongodb/specifications). Хоча модуль можна використовувати безпосередньо, бібліотека дає мінімальні накладні витрати і має бути загальною залежністю для більшої частини додатків, побудованих з MongoDB.

На рівень нижче бібліотеки розташовується PHP-модуль, який розповсюджується через репозиторій [» PECL](https://pecl.php.net/package/mongodb). Модуль утворює сполучний прошарок між PHP і системними бібліотеками ([» libmongoc](https://github.com/mongodb/mongo-c-driver) [» libbson](https://github.com/mongodb/mongo-c-driver/tree/master/src/libbson) і [» libmongocrypt](https://github.com/mongodb/libmongocrypt)). Цей публічний API пропонує тільки саму базову функціональність:

-   Управління з'єднанням
-   BSON кодування та декодування
-   Серіалізація документа об'єкта (для підтримки бібліотек ODM)
-   Виконання команд, запити та запис операцій
-   Обробка курсорів для команд та результатів запиту

**Вихідний код драйвера та проекти JIRA**

| Проект | GitHub | JIRA |
| --- | --- | --- |
| PHP бібліотека | [» mongodb/mongo-php-library](https://github.com/mongodb/mongo-php-library) | [» PHPLIB](https://jira.mongodb.org/browse/PHPLIB) |
| PHP-модуль | [» mongodb/mongo-php-driver](https://github.com/mongodb/mongo-php-driver) | [» PHPC](https://jira.mongodb.org/browse/PHPC) |
