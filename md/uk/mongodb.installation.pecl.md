---
navigation:
  - mongodb.installation.html: « Установка
  - mongodb.installation.homebrew.html: Установка драйвера PHP MongoDB на macOS помощью Homebrew »
  - index.html: PHP Manual
  - mongodb.installation.html: Установка
title: Встановлення драйвера PHP MongoDB за допомогою PECL
---
## Встановлення драйвера PHP MongoDB за допомогою PECL

Інформація щодо встановлення цього модуля PECL може бути знайдена у розділі посібника [Установка PECL модулей](install.pecl.html). Додаткову інформацію, таку як нові версії, завантаження, вихідні файли, інформація про розробника та CHANGELOG, можна знайти тут: [» https://pecl.php.net/package/mongodb](https://pecl.php.net/package/mongodb)

Користувачі Linux, Unix та macOS можуть використовувати наступну команду для встановлення драйвера:

$ sudo pecl install mongodb

Якщо на вашій системі встановлено кілька версій PHP (наприклад, для macOS: установка за замовчуванням, Homebrew та [» XAMPP](https://www.apachefriends.org/)), зверніть увагу, що кожна з них має власну команду [pecl](install.pecl.html) та файли php.ini. Крім того, кожне оточення PHP (наприклад CLI, web) може використовувати окремі файли php.ini.

Встановлення драйвера за допомогою PECL використовує вбудовані бібліотеки [» libbson](https://github.com/mongodb/mongo-c-driver/tree/master/src/libbson) і [» libmongoc](https://github.com/mongodb/mongo-c-driver) і спробує налаштувати їх автоматично.

> **Зауваження**: Якщо процес встановлення не зможе знайти бібліотеку SSL, переконайтеся, що встановлені пакети розробок (такі як `libssl-dev`) та пакет [» pkg-config](https://en.wikipedia.org/wiki/Pkg-config). Якщо це не допоможе, то зробіть [ручную установку](mongodb.installation.manual.html)

І, нарешті, додайте наступний рядок у файл php.ini для кожного оточення, в якому ви збираєтеся використовувати драйвер:

extension=mongodb.so
