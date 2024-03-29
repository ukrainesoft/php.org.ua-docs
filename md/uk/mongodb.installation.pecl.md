---
navigation:
  - mongodb.installation.md: « Встановлення
  - mongodb.installation.homebrew.md: Установка драйвера PHP MongoDB на macOS за допомогою Homebrew »
  - index.md: PHP Manual
  - mongodb.installation.md: Установка
title: Встановлення драйвера PHP MongoDB за допомогою PECL
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Встановлення драйвера PHP MongoDB за допомогою PECL

Інформація щодо встановлення цього модуля PECL може бути знайдена у розділі посібника [Встановлення PECL модулів](install.pecl.md). Додаткову інформацію, таку як нові версії, завантаження, вихідні файли, інформація про розробника та CHANGELOG, можна знайти тут: [» https://pecl.php.net/package/mongodb](https://pecl.php.net/package/mongodb)

Користувачі Linux, Unix та macOS можуть використовувати наступну команду для встановлення драйвера:

$ sudo pecl install mongodb

На системах з кількома встановленими версіями PHP (наприклад, для macOS: установка за замовчуванням, Homebrew та [» XAMPP](https://www.apachefriends.org/)) кожна версія PHP матиме власну команду [pecl](install.pecl.md) та файл (або файли) php.ini. Крім того, кожне оточення PHP (наприклад CLI, web) може використовувати окремі файли php.ini.

Починаючи з версії драйвера 1.17.0 PECL буде вимагати різні настройки `configure`. Встановити драйвер із налаштуваннями за замовчуванням у неінтерактивному сценарії можна з переданим на вхід порожнім рядком для команди `yes`, відокремленої символом вертикальної межі від команди `pecl install` :

$ yes '' | sudo pecl install mongodb

Повний список параметрів, що підтримуються `configure` можна знайти у файлі `package.xml`, включеному до пакету PECL. Щоб інсталювати драйвер зі специфічними параметрами `configure` в неінтерактивному сценарії може бути вказано параметр `--configureoptions` для команди `pecl install` :

$ sudo pecl install --configureoptions='with-mongodb-system-libs="yes" enable-mongodb-developer-flags="no"' mongodb

За замовчуванням інсталяція драйвера через PECL використовуватиме вбудовані версії модулів: [» libbson](https://github.com/mongodb/mongo-c-driver/tree/master/src/libbson) [» libmongoc](https://github.com/mongodb/mongo-c-driver) [» libmongocrypt](https://github.com/mongodb/libmongocrypt) і спробує налаштувати їх автоматично.

> **Зауваження**: Якщо процес встановлення не зможе знайти бібліотеку SSL, переконайтеся, що встановлені пакети для розробки (такі як `libssl-dev`) та пакет [» pkg-config](https://en.wikipedia.org/wiki/Pkg-config). Якщо це не допоможе, то зробіть [ручне встановлення](mongodb.installation.manual.md)

І нарешті, додайте наступний рядок у файл php.ini для кожного оточення, в якому буде використано драйвер:

extension=mongodb.so
