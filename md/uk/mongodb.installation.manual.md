---
navigation:
  - mongodb.installation.windows.md: « Установка драйвера PHP MongoDB под Windows
  - mongodb.configuration.md: Налаштування під час виконання »
  - index.md: PHP Manual
  - mongodb.installation.md: Установка
title: Складання драйвера PHP MongoDB з вихідного коду
---
## Складання драйвера PHP MongoDB з вихідного коду

Розробники драйверів і людей, зацікавлені в найсвіжіших версіях, можуть зібрати драйвер з вихідних кодів, які знаходяться тут: [» GitHub](https://github.com/mongodb/mongo-php-driver). Запустіть наступні команди для клонування та складання проекту:

$ git clone [https://github.com/mongodb/mongo-php-driver.git](https://github.com/mongodb/mongo-php-driver.git)$ cd mongo-php-driver $ git submodule update --init $phpize $./configure $ make all $ sudo make install

Якщо у вашій системі встановлено кілька версій PHP (наприклад, для macOS установка за замовчуванням, Homebrew, [» XAMPP](https://www.apachefriends.org/)), зверніть увагу, що кожна версія PHP має свою команду [phpize](install.pecl.phpize.md) та php.ini файл(и). Крім того, кожне оточення PHP (наприклад, CLI, web) може використовувати окремі php.ini файли.

За промовчанням драйвер використовуватиме вбудовану версію [» libbson](https://github.com/mongodb/mongo-c-driver/tree/master/src/libbson) [» libmongoc](https://github.com/mongodb/mongo-c-driver) і [» libmongocrypt](https://github.com/mongodb/libmongocrypt) та спробує налаштувати їх самостійно. Якщо ці бібліотеки вже встановлені в системі, ви можете повідомити драйвер про це за допомогою аргументу `--with-libbson=yes --with--libmongoc=yes` команди `configure`. Починаючи з версії 1.7.0 модуля ці аргументи застаріли, і ви повинні використовувати замість них `--with-mongodb-system-libs=yes`

Повний список опцій команди `configure` можна отримати за допомогою **configure --help**

При використанні вбудованих версій libbson і libmongoc драйвер також спробує вибрати бібліотеку SSL відповідно до опції `--with-mongodb-ssl` команди `configure`. За умовчанням це `--with-mongodb-ssl=auto`, що призведе до пошуку у такому порядку: Secure Transport (тільки macOS), OpenSSL, LibreSSL. Також ви можете явно вказати `openssl` `libressl` або `darwin`

> **Зауваження**
> 
> Якщо процес встановлення не зможе знайти бібліотеку SSL, переконайтеся, що встановлені пакети розробок (такі як `libssl-dev`) та пакет [» pkg-config](https://en.wikipedia.org/wiki/Pkg-config)
> 
> При використанні Homebrew для macOS звичайна ситуація, коли встановлено кілька різних версій OpenSSL. Для використання саме тієї версії, яка вам потрібна, відповідним чином установіть змінну оточення `PKG_CONFIG_PATH`. Вона використовуватиметься `pkg-config` для визначення шляху пошуку. Якщо не використовується `pkg-config`, то можна використовувати `configure` з ключем `--with-openssl-dir=DIR` (лише для OpenSSL).

На останньому, фінальному етапі, **make install** виведе шлях, яким було зібрано модуль mongodb.so. Наприклад так:

Installing shared extensions: /usr/lib/php/extensions/debug-non-zts-20151012/

Переконайтеся, що директива [extensiondir](ini.core.md#ini.extension-dir) файлу php.ini вказує на каталог, у якому є бібліотека mongodb.so. Перевірити значення цієї директиви можна так:

$php-i | grep extensiondir extensiondir => /usr/lib/php/extensions/debug-non-zts-20151012 => /usr/lib/php/extensions/debug-non-zts-20151012

Якщо директорії відрізняються, змініть значення [extensiondir](ini.core.md#ini.extension-dir) у php.ini або просто перемістіть mongodb.so у потрібну директорію.

Додайте наступний рядок до файлу php.ini для кожного оточення, в якому ви збираєтеся використовувати драйвер:

extension=mongodb.so
