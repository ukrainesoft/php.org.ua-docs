---
navigation:
  - mongodb.installation.windows.md: « Встановлення драйвера PHP MongoDB під Windows
  - mongodb.configuration.md: Налаштування під час виконання »
  - index.md: PHP Manual
  - mongodb.installation.md: Установка
title: Складання драйвера PHP MongoDB з вихідного коду
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Складання драйвера PHP MongoDB з вихідного коду

Розробники драйверів та зацікавлені у найсвіжіших версіях користувачі можуть зібрати драйвер із вихідних кодів: [» GitHub](https://github.com/mongodb/mongo-php-driver). Запустіть наступні команди для клонування та складання проекту:

$ git clone[https://github.com/mongodb/mongo-php-driver.git](https://github.com/mongodb/mongo-php-driver.git)$ cd mongo-php-driver $ git submodule update --init $ phpize $ ./configure $ make all $ sudo make install

У системах з кількома встановленими версіями PHP (наприклад, macOS: стандартна установка, Homebrew, [» XAMPP](https://www.apachefriends.org/)) у кожної версії PHP буде своя команда [phpize](install.pecl.phpize.md) та файл (або файли) php.ini. Крім того, кожне оточення PHP (наприклад CLI, web) може використовувати окремі файли php.ini.

За промовчанням драйвер використовуватиме вбудовані версії модулів [» libbson](https://github.com/mongodb/mongo-c-driver/tree/master/src/libbson) [» libmongoc](https://github.com/mongodb/mongo-c-driver) і [» libmongocrypt](https://github.com/mongodb/libmongocrypt) та спробує налаштувати їх автоматично. Якщо ці модулі вже встановлені в системі, драйвер може їх використовувати, передавши параметр `--with-mongodb-system-libs=yes`команде`configure`

Повний перелік параметрів команди `configure` можна отримати, запустивши: **configure --help**

При використанні вбудованих версій модулів libmongoc і libmongocrypt драйвер також спробує вибрати модуль SSL відповідно до параметра `--with-mongodb-ssl` команди `configure`. Починаючи з версії драйвера 1.17.0 за замовчуванням буде віддано перевагу бібліотеці OpenSSL. Попередні версії драйвера на системах з macOS за промовчанням вибирали Secure Transport, а на всіх інших платформах — OpenSSL.

> **Зауваження** :
> 
> Якщо процес встановлення не зможе знайти бібліотеку SSL, переконайтеся, що встановлені пакети для розробки (такі як `libssl-dev`) та пакет [» pkg-config](https://en.wikipedia.org/wiki/Pkg-config)
> 
> При використанні Homebrew для macOS звичайна ситуація, коли встановлено кілька різних версій OpenSSL. Для використання саме тієї версії, яка вам потрібна, відповідним чином установіть змінну оточення `PKG_CONFIG_PATH`. Вона використовуватиметься `pkg-config` для визначення шляху пошуку. Якщо не використовується `pkg-config`, то можна використовувати `configure` з ключем `--with-openssl-dir=DIR` (лише OpenSSL).

На останньому, фінальному етапі, **make install** виведе шлях, яким було зібрано модуль mongodb.so. Наприклад так:

Installing shared extensions: /usr/lib/php/extensions/debug-non-zts-20220829/

Переконайтеся, що директива [extension\_dir](ini.core.md#ini.extension-dir) файлу php.ini вказує на каталог, у якому є модуль mongodb.so. Перевірити значення цієї директиви можна так:

$ php -i | grep extension\_dir extension\_dir => /usr/lib/php/extensions/debug-non-zts-20220829 => /usr/lib/php/extensions/debug-non-zts-20220829

Якщо директорії відрізняються, змініть значення [extension\_dir](ini.core.md#ini.extension-dir) у php.ini або просто перемістіть mongodb.so у потрібну директорію.

І, нарешті, додайте наступний рядок у файл php.ini для кожного оточення, в якому ви збираєтеся використовувати драйвер:

extension=mongodb.so
