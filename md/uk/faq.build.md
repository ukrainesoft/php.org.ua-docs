Проблеми збирання

-   [« Установка](faq.installation.html)
    
-   [Использование PHP »](faq.using.html)
    
-   [PHP Manual](index.html)
    
-   [ЧАВО](faq.html)
    
-   Проблеми збирання
    

# Проблеми збирання

У цьому розділі зібрані найбільш загальні помилки, що виникають на етапі збирання.

1.  [Я получил последнюю версию PHP, используя анонимный доступ к Git, но в нём нет конфигурационного скрипта!](#faq.build.configure)
2.  [У меня возникают проблемы при конфигурировании PHP для работы с Apache. Он говорит, что не может найти httpd.h, хотя файл находится точно там, где я сказал!](#faq.build.configuring)
3.  [Во время конфигурации PHP (./configure) вы наталкиваетесь на ошибку, схожую со следующей: checking lex output file root... ./configure: lex: command not found configure: error: cannot find output from lex; giving up](#faq.build.lex)
4.  [Когда я пытаюсь запустить Apache, я получаю следующее сообщение: fatal: relocation error: file /path/to/libphp4.so: symbol ap\_block\_alarms: referenced symbol not found](#faq.build.apache-sharedcore)
5.  [Когда я запускаю configure, он говорит, что не может найти файлы include или библиотеку для GD, gdbm или какого-либо другого пакета!](#faq.build.not-found)
6.  [При компиляции файла language-parser.tab.c мне выдаются ошибки, говорящие yytname undeclared.](#faq.build.yytname)
7.  [Когда я запускаю make, похоже, он выполняется нормально, но на конечной линковке жалуется, что не может найти некоторые файлы.](#faq.build.link)
8.  [При компоновке PHP, он жалуется на некоторые неопределённые ссылки.](#faq.build.undefined)
9.  [Я следовал всем шагам по установке модульной версии для Apache на Unix, но мои PHP-скрипты выводятся в браузере или я получаю запрос сохранить файл.](#faq.build.not-running)
10.  [В документации рекомендуется использовать: --activate-module=src/modules/php4/libphp4.a, но такой файл не существует, поэтому я заменил это на --activate-module=src/modules/php4/libmodphp4.a и оно не работает!? Что происходит?](#faq.build.activate-module)
11.  [Когда я пытаюсь собрать Apache c PHP в виде статического модуля, используя --activate-module=src/modules/php4/libphp4.a он говорит, что мой компилятор не ANSI-совместимый.](#faq.build.ansi)
12.  [Когда я пытаюсь собрать PHP с помощью --with-apxs, я получаю странное сообщение об ошибке.](#faq.build.apxs)
13.  [Во время выполнения make я очень быстро получаю ошибки и множество всяких RUSAGE\_.](#faq.build.microtime)
14.  [При компиляции PHP с MySQL, configure выполняется нормально, но во время make я получаю ошибку типа следующей: ext/mysql/libmysqlclient/my\_tempnam.o(.text+0x46): In function my\_tempnam': /php4/ext/mysql/libmysqlclient/my\_tempnam.c:103: the use of tempnam' is dangerous, better use mkstemp', в чём дело?](#faq.build.mysql.tempnam)
15.  [Я хочу обновить мой PHP. Где я могу найти строку ./configure, которая была использована для моей текущей PHP установки?](#faq.build.upgrade)
16.  [При сборке PHP с библиотекой GD, либо выдаются странные ошибки компиляции, либо ошибки сегментации (segfaults) при выполнении.](#faq.build.gdlibs)
17.  [При компиляции PHP я, кажется, получаю случайные ошибки, например она зависает. Я использую Solaris, если это имеет значение.](#faq.installation.needgnu)

**Я отримав останню версію PHP, використовуючи анонімний доступ до Git, але немає конфігураційного скрипта!**

Вам потрібний встановлений пакет GNU autoconf для того, щоб згенерувати конфігураційний скрипт із configure.in. Після отримання вихідних з Git сервера просто запустіть **./buildconf** у директорії верхнього рівня. (Також, якщо ви запускаєте **configure** без опції `--enable-maintainer-mode`, то конфігураційний скрипт не буде перебудовано автоматично при зміні файлу configure.in, тому вам необхідно робити це вручну, коли ви помітите, що configure.in змінився. Один із симптомів - поява таких речей як @VARIABLE@ у вашому Makefile після виконання configure або config.status.)

**У мене виникають проблеми з конфігурацією PHP для роботи з Apache. Він каже, що не може знайти httpd.h, хоча файл знаходиться саме там, де я сказав!**

Для configure/setup скрипта необхідно вказати директорію верхнього рівня, в якій знаходяться вихідні коди Apache. Це означає, що вам потрібно поставити **\-with-apache=/path/to/apache**, а *не* **\-with-apache=/path/to/apache/src**

\*\*Під час конфігурації PHP (`./configure`) Ви відштовхуєтеся на помилку, схожу з наступною:

checking lex output file root... ./configure: lex: command not found  
configure: error: cannot find output from lex; giving up

Не забудьте уважно прочитати інструкції з [установке](install.unix.html) та зауважте, що для компіляції PHP вам потрібно встановити як flex, так і bison. Залежно від ваших налаштувань, встановіть bison і flex або з вихідних кодів, або з пакетів, наприклад, RPM.

\*\*Коли я намагаюся запустити Apache, я отримую наступне повідомлення:

fatal: relocation error: файл /path/to/libphp4.so:  
symbol apblockalarms: referenced symbol not found

Ця помилка зазвичай з'являється, якщо ядро ​​Apache було скомпілюване як бібліотека DSO (Dynamic Shared Object), що розділяється. Спробуйте переконфігурувати Apache, використовуючи принаймні такі прапори:

\-enable-shared=max --enable-rule=SHAREDCORE

Для більш детальної інформації читайте файл INSTALL у директорії верхнього рівня або [»  страницу руководства Apache по DSO](http://httpd.apache.org/docs/current/dso.html)

**Коли я запускаю configure, він каже, що не може знайти файли include або бібліотеку для GD, gdbm або іншого пакета!**

Ви можете зробити так, що скрипт configure буде шукати файли заголовків або бібліотеки в нестандартних місцях, задавши додаткові прапори для препроцесора і компонувальника, такі як:

```
CPPFLAGS=-I/path/to/include LDFLAGS=-L/path/to/library ./configure
```

Якщо ви використовуєте csh-подібну оболонку (навіщо?), Це буде:

```
env CPPFLAGS=-I/path/to/include LDFLAGS=-L/path/to/library ./configure
```

**При компіляції файлу language-parser.tab.c мені видаються помилки, які говорять `yytname undeclared`**

Вам потрібно оновити вашу версію Bison. Останню версію можна знайти на [» http://www.gnu.org/software/bison/bison.html](http://www.gnu.org/software/bison/bison.html)

**Коли я запускаю **make**, схоже, він виконується нормально, але на кінцевому лінківці скаржиться, що не може знайти деякі файли.**

Деякі старі версії make помилково не поміщають скомпіловані файли в піддиректорію функцій у тій же директорії. Спробуйте виконати **сп .o functions** а потім перезапустити **make**. Якщо це допомогло, вам дійсно потрібно встановити свіжу версію GNU make.

**При компонуванні PHP він скаржиться на деякі невизначені посилання.**

Подивіться на рядок для компонування та переконайтеся, що всі необхідні бібліотеки додані наприкінці. Часто забувають '-ldl' і бібліотеки, необхідні підтримки включних вручну баз даних.

Деякі люди також повідомляють, що при компонуванні з Apache їм довелося додати '-ldl' одразу після libphp4.a.

**Я дотримувався всіх кроків для встановлення модульної версії для Apache на Unix, але мої PHP-скрипти виводяться в браузері або я отримую запит зберегти файл.**

Це означає, що модуль PHP з якоїсь причини не викликається. Перед тим, як звертатися за допомогою, перевірте три речі:

-   Переконайтеся, що бінарник httpd, що запускається вами, дійсно новий, щойно побудований httpd. Для цього спробуйте запустити: `/path/to/binary/httpd -l` Якщо ви не бачите modphp4.c у списку, то ви запускаєте не той бінарник. Знайдіть та встановіть правильний бінарник.
-   Переконайтеся, що ви додали правильний Mime Type до одного з ваших `Apache .conf` файлів. Це повинно бути: `AddType application/x-httpd-php .php` Також переконайтеся, що цей рядок AddType не потрапив усередину або блоку, так як це не дасть їй працювати з місцезнаходженням тестового скрипта.
-   Нарешті, між Apache 1.2 та Apache 1.3 розташування конфігураційних файлів Apache за умовчанням змінилося. Вам потрібно перевірити, чи дійсно читається той конфігураційний файл, до якого ви додали рядок AddType. Ви можете внести очевидну синтаксичну помилку до вашого httpd.conf файлу або будь-якої іншої помітної зміни, яка покаже вам, що читається правильний файл.

**У документації рекомендується використовувати: `--activate-module=src/modules/php4/libphp4.a`, але такий файл не існує, тому я замінив це на `--activate-module=src/modules/php4/libmodphp4.a` і воно не працює!? Що відбувається?**

Зауважте, що файл libphp4.a не повинен існувати. Він буде створений у процесі!

**Коли я намагаюся зібрати Apache з PHP у вигляді статичного модуля, використовуючи `--activate-module=src/modules/php4/libphp4.a` він каже, що мій компілятор не ANSI-сумісний.**

Повідомлення про помилку вводить в оману; це виправлено у свіжих версіях Apache.

**Коли я намагаюся зібрати PHP за допомогою **\-with-apxs**я отримую дивне повідомлення про помилку.**

Перевірте три речі. По-перше, з якоїсь причини, коли Apache створює Perl скрипт apxs, він виходить без правильного компілятора та змінних, які задають прапори. Знайдіть ваш apxs скрипт (спробуйте команду **which apxs**), іноді він встановлений як /usr/local/apache/bin/apxs або /usr/sbin/apxs. Відкрийте його і знайдіть рядки, схожі на такі:

```
my $CFG_CFLAGS_SHLIB  = ' ';          # substituted via Makefile.tmpl
my $CFG_LD_SHLIB      = ' ';          # substituted via Makefile.tmpl
my $CFG_LDFLAGS_SHLIB = ' ';          # substituted via Makefile.tmpl
```

Якщо вони так і виглядають, ви знайшли вашу проблему. Вони можуть містити лише прогалини або інші неправильні значення, такі як q(). Змініть ці рядки на:

```
my $CFG_CFLAGS_SHLIB  = '-fpic -DSHARED_MODULE'; # substituted via Makefile.tmpl
my $CFG_LD_SHLIB      = 'gcc';                   # substituted via Makefile.tmpl
my $CFG_LDFLAGS_SHLIB = q(-shared);              # substituted via Makefile.tmpl
```

Друга можлива проблема виникає лише на Red Hat 6.1 та 6.2. Скрипт apxs, що поставляється з Red Hat, зламаний. Шукайте цей рядок:

```
my $CFG_LIBEXECDIR    = 'modules';         # substituted via APACI install
```

Якщо ви знайшли вищенаведений рядок, змініть його на наступне:

```
my $CFG_LIBEXECDIR    = '/usr/lib/apache'; # substituted via APACI install
```

І останнє, якщо ви переконфігуруєте/встановлюєте Apache, запустіть **make clean** після **./configure** і перед **make**

**Під час виконання **make** я дуже швидко отримую помилки і безліч всяких `RUSAGE_`**

При виконанні **make** під час встановлення, якщо ви стикаєтеся з проблемами, схожими на наступне:

```
microtime.c: In function `php_if_getrusage':
microtime.c:94: storage size of `usg' isn't known
microtime.c:97: `RUSAGE_SELF' undeclared (first use in this function)
microtime.c:97: (Each undeclared identifier is reported only once
microtime.c:97: for each function it appears in.)
microtime.c:103: `RUSAGE_CHILDREN' undeclared (first use in this function)
make[3]: *** [microtime.lo] Error 1
make[3]: Leaving directory `/home/master/php-4.0.1/ext/standard'
make[2]: *** [all-recursive] Error 1
make[2]: Leaving directory `/home/master/php-4.0.1/ext/standard'
make[1]: *** [all-recursive] Error 1
make[1]: Leaving directory `/home/master/php-4.0.1/ext'
make: *** [all-recursive] Error 1
```

Ваша система зламана. Ви повинні виправити файли /usr/include, встановивши пакет glibc-devel, який відповідає вашому glibc. Це абсолютно не залежить від PHP. Для доказу спробуйте наступний простий тест:

```
$ cat >test.c <<X
#include <sys/resource.h>
X
$ gcc -E test.c >/dev/null
```

Якщо видаються помилки, ваші include файли зіпсовані.

*При компіляції PHP з MySQL, configure виконується нормально, але під час `make` я отримую помилку типу наступного: *ext/mysql/libmysqlclient/mytempnam.o(.text+0x46): In function mytempnam': /php4/ext/mysql/libmysqlclient/mytempnam.c:103: use of tempnam' is dangerous, better use mkstemp'*, в чому справа?*

По-перше, важливо розуміти, що це `Warning` (попередження), а чи не фатальна помилка. Так як це останнє, що виводиться під час `make`, вона може виглядати як фатальна помилка, але це не так. Звісно, ​​якщо ваш компілятор помирає на попередженнях, (Warnings), тоді так. Також майте на увазі, що підтримка MySQL включена за умовчанням.

> **Зауваження**
> 
> Починаючи з PHP 4.3.2, ви також будете бачити наступний текст після того, як збірка (make) завершиться:
> 
> Build complete.  
> (It is safe to ignore warnings про tempnam and tmpnam).  
> (Складання завершено, можна безпечно ігнорувати  
> попередження про tempnam та tmpnam.)

**Я хочу оновити мій PHP. Де я можу знайти рядок **./configure**яка була використана для моєї поточної PHP установки?**

Або дивіться файл config.nice у дереві вихідних записів вашої поточної PHP установки, або, якщо це недоступно, просто виконайте скрипт:

```php
<?php phpinfo(); ?>
```

На початку виводу буде рядок **./configure**, яка була використана для збирання поточного PHP.

**При складанні PHP з бібліотекою GD або видаються дивні помилки компіляції або помилки сегментації (segfaults) при виконанні.**

Переконайтеся, що ваша бібліотека GD і PHP компонуються з тими самими залежними бібліотеками (наприклад, libpng).

**При компіляції PHP я, здається, отримую випадкові помилки, наприклад, вона зависає. Я використовую Solaris якщо це має значення.**

Використання не утиліт GNU під час компіляції PHP може викликати проблеми. Щоб бути впевненим, що компіляція PHP буде працювати, використовуйте утиліти GNU. Наприклад, у Solaris, використання SunOS BSD-сумісної або Solaris версії `sed` не працюватиме, а GNU або Sun POSIX (xpg4) версії `sed` буде. Посилання: [» GNU sed](http://www.gnu.org/software/sed/sed.html) [» GNU flex](http://www.gnu.org/software/flex/flex.html), and [» GNU bison](http://www.gnu.org/software/bison/bison.html)