Список опцій командного рядка

-   [Основні відмінності від інших реалізацій SAPI](features.commandline.differences.md)
    
-   [Использование »](features.commandline.usage.md)
    
-   [PHP Manual](index.md)
    
-   [Використання PHP у командному рядку](features.commandline.md)
    
-   Список опцій командного рядка
    

## Список опцій командного рядка

Список опцій командного рядка, що надаються PHP, можуть бути отримані будь-якої миті, запустивши PHP з ключем **х**

```
Usage: php [options] [-f] <file> [--] [args...]
   php [options] -r <code> [--] [args...]
   php [options] [-B <begin_code>] -R <code> [-E <end_code>] [--] [args...]
   php [options] [-B <begin_code>] -F <file> [-E <end_code>] [--] [args...]
   php [options] -- [args...]
   php [options] -a

  -a               Run interactively
  -c <path>|<file> Look for php.ini file in this directory
  -n               No php.ini file will be used
  -d foo[=bar]     Define INI entry foo with value 'bar'
  -e               Generate extended information for debugger/profiler
  -f <file>        Parse and execute <file>.
  -h               This help
  -i               PHP information
  -l               Syntax check only (lint)
  -m               Show compiled in modules
  -r <code>        Run PHP <code> without using script tags <?..?>
  -B <begin_code>  Run PHP <begin_code> before processing input lines
  -R <code>        Run PHP <code> for every input line
  -F <file>        Parse and execute <file> for every input line
  -E <end_code>    Run PHP <end_code> after processing all input lines
  -H               Hide any passed arguments from external tools.
  -S <addr>:<port> Run with built-in web server.
  -t <docroot>     Specify document root <docroot> for built-in web server.
  -s               Output HTML syntax highlighted source.
  -v               Version number
  -w               Output source with stripped comments and whitespace.
  -z <file>        Load Zend extension <file>.

  args...          Arguments passed to script. Use -- args when first argument
                   starts with - or script is read from stdin

  --ini            Show configuration file names

  --rf <name>      Show information about function <name>.
  --rc <name>      Show information about class <name>.
  --re <name>      Show information about extension <name>.
  --rz <name>      Show information about Zend extension <name>.
  --ri <name>      Show configuration for extension <name>.
```

**Опції, доступні з командного рядка**

| Опция                                                                                                                                          | Полное название | Описание |
|------------------------------------------------------------------------------------------------------------------------------------------------|-----------------|----------|
| а                                                                                                                                              | \-interactive   |          |
| Запустити PHP в режимі онлайн. Для отримання додаткової інформації дивіться розділ [Інтерактивна консоль](features.commandline.interactive.md) |                 |          |

b | -bindpath |

Шлях зв'язування бібліотек (Bind Path) для зовнішнього режиму FASTCGI Server (лише CGI).

C | -no-chdir |

Не змінювати поточну директорію на директорію скрипта (лише для CGI).

q | -no-header |

Тихий режим. Пригнічує виведення заголовків HTTP (лише CGI).

T | -Тімінг |

Виміряти час виконання скрипту, повтореного count разів (тільки для CGI).

з | -php-ini |

Вказує або директорію, в якій потрібно шукати конфігураційний файл php.ini, або користувальницький `INI`файл (назва якого може відрізнятися від стандартного php.ini), наприклад:

```
$ php -c /custom/directory/ my_script.php

$ php -c /custom/directory/custom-file.ini my_script.php
```

Якщо ця опція не вказана, пошук php.ini буде здійснено в [местах по умолчанию](configuration.file.md)

n | -no-php-ini |

Повністю ігнорувати php.ini.

d | -define |

Встановлює значення користувача для кожної з конфігураційних опцій, доступних у php.ini. Синтаксис виглядає так:

```
-d configuration_directive[=value]
```

```
# Если значение опущено, то соответствующей опции будет присвоено значение "1"
$ php -d max_execution_time
        -r '$foo = ini_get("max_execution_time"); var_dump($foo);'
string(1) "1"

# Указание пустого значения установит соответствующую опцию значением ""
php -d max_execution_time=
        -r '$foo = ini_get("max_execution_time"); var_dump($foo);'
string(0) ""

# Конфигурационная переменная будет установлена любым значением, указанным после символа '='
$  php -d max_execution_time=20
        -r '$foo = ini_get("max_execution_time"); var_dump($foo);'
string(2) "20"
$  php
        -d max_execution_time=doesntmakesense
        -r '$foo = ini_get("max_execution_time"); var_dump($foo);'
string(15) "doesntmakesense"
```

e | -profile-info |

Увімкнути режим розширеної інформації, що використовується налагоджувачем/профайлером.

f | -file |

Парсит та виконує файл, вказаний у опції **ф**. Цей параметр необов'язковий і може бути опущений - досить просто вказати ім'я файлу, що запускається.

h і -? | -help та --usage | Виводить список опцій командного рядка з однорядковим описом того, що вони роблять. | | i | -info | Викликає [phpinfo()](function.phpinfo.md) та виводити її результат. Якщо PHP працює некоректно, рекомендується виконати **php -i** та подивитися, чи виводяться повідомлення про помилки до або замість інформаційних таблиць. Враховуйте, що у разі використання CGIМодуль весь висновок буде у форматі HTML і, як наслідок, дуже великий. | | l | -syntax-check |

Надає зручний спосіб перевірки заданого PHP-коду на наявність синтаксичних помилок. У разі успішної перевірки буде надруковано таку фразу: "`No syntax errors detected in <filename>`", а код повернення дорівнюватиме `0`. При невдалій перевірці буде виведено`Errors parsing <filename>`разом із внутрішніми повідомленнями парсера, а код повернення дорівнюватиме `-1`

Ця опція не виявлятиме фатальних помилок (наприклад, виклик невизначених функцій). Використовуйте опцію **ф**якщо ви хочете перевірити код на наявність фатальних помилок.

> **Зауваження**
> 
> Ця опція не працює з опцією **р**

м | -модулі |

**Приклад #1 Виведення вбудованих (і завантажених) модулів PHP та Zend**

```
$ php -m
[PHP Modules]
xml
tokenizer
standard
session
posix
pcre
overload
mysql
mbstring
ctype

[Zend Modules]
```

r | -Run |

Дозволяє виконувати PHP-код, вказаний безпосередньо у командному рядку. Відкриваючі та закриваючі PHP-теги (`<?php` і `?>` *не потрібні* і будуть призводити до синтаксичної помилки, якщо вони присутні.

> **Зауваження**
> 
> При використанні цього ключа слід бути дуже обережним і уникати непорозумінь, пов'язаних з автоматичним встановленням змінних оточення.
> 
> **Приклад #2 Помилка синтаксису під час використання подвійних лапок**
> 
> ```
> $ php -r "$foo = get_defined_constants();"
> PHP Parse error:  syntax error, unexpected '=' in Command line code on line 1
> 
> Parse error: syntax error, unexpected '=' in Command line code on line 1
> ```
> 
> Проблема тут полягає в тому, що sh/bash виконує автоматичну підстановку змінних у випадку, якщо використовуються подвійні лапки (`"`). Оскільки змінна $foo навряд чи визначена, вона замінюється порожнім рядком, що призводить до того, що переданий PHP-код для виконання виглядає так:
> 
> ```
> $ php -r " = get_defined_constants();"
> ```
> 
> Правильним рішенням у цьому випадку буде використання одинарних лапок `'`, оскільки автоматична підстановка змінних, укладених в одинарні лапки, sh/bash не відбувається.
> 
> **Приклад #3 Використання одинарних лапок для запобігання підстановці змінних у консолі**
> 
> ```
> $ php -r '$foo = get_defined_constants(); var_dump($foo);'
> array(370) {
>   ["E_ERROR"]=>
>   int(1)
>   ["E_WARNING"]=>
>   int(2)
>   ["E_PARSE"]=>
>   int(4)
>   ["E_NOTICE"]=>
>   int(8)
>   ["E_CORE_ERROR"]=>
>   [...]
> ```
> 
> При використанні оболонки, яка відрізняється від sh/bash, можуть виникнути інші проблеми. У такому випадку необхідно створити звіт про помилку, що виникла на сайті [» https://github.com/php/php-src/issues](https://github.com/php/php-src/issues). Ви можете зіткнутися з проблемами при спробі отримати доступ до змінних оболонки або при роботі з зворотними слішами, що екранують. Тепер ви попереджені!

> **Зауваження**
> 
> Ключ **р** доступний у CLI SAPI, але недоступний *CGI* SAPI.

> **Зауваження**
> 
> Ця опція призначена лише для найпростішого коду. Тому деякі конфігураційні директиви (наприклад, [autoprependfile](ini.core.html#ini.auto-prepend-file) і [autoappendfile](ini.core.html#ini.auto-append-file)) у цьому режимі будуть проігноровані.

B | -process-begin |

Виконуваний PHP код перед обробкою потоку введення (stdin).

R | -process-code |

PHP-код, який виконується для кожного рядка введення.

У цьому режимі є дві спеціальні змінні: $ argn і $ argi. $argn містить рядок, який PHP обробляє в даний момент, а $argi містить номер цього рядка.

F | -process-file |

PHP-файл для кожного рядка введення.

E | -process-end |

PHP-код, який виконується після обробки введення.

**Приклад #4 Використання опцій **У** **Р** і **Е** для підрахунку кількості рядків у проекті.**

```
$ find my_proj | php -B '$l=0;' -R '$l += count(@file($argn));' -E 'echo "Всего строк: $l\n";'
Всего строк: 37328
```

S | -server |

Запускає [вбудований веб-сервер](features.commandline.webserver.md)

t | -docroot | Вказує корінь документа для [вбудованого веб-сервера](features.commandline.webserver.md). s | -syntax-highlight і --syntax-highlighting |

Показати вихідний код із підсвічуванням синтаксису.

Ця опція використовує внутрішній механізм для аналізу файлу і запису в стандартний потік виведення підсвіченої версії цього файлу. Врахуйте, що все, що вона робить, це генерує блок `<code> [...] </code>` HTML-тегів, без HTML-заголовків.

> **Зауваження**
> 
> Ця опція несумісна з опцією **р**

у | -version |

**Приклад #5 Використання **в** для отримання типу SAPI та версії PHP та Zend**

```
$ php -v
PHP 5.3.1 (cli) (built: Dec 11 2009 19:55:07)
Copyright (c) 1997-2009 The PHP Group
Zend Engine v2.3.0, Copyright (c) 1998-2009 Zend Technologies
```

w | -Strip |

Показати вихідний код без коментарів та пробілів.

> **Зауваження**
> 
> Ця опція несумісна з опцією **р**

z | -Zend-Extension |

Завантажує модуль Zend. Якщо передано лише ім'я файлу, PHP спробує завантажити цей модуль зі шляху бібліотек за промовчанням (зазвичай вказується в /etc/ld.so.conf у системах Linux). Передача файлу з абсолютним шляхом не використовуватиме шлях пошуку бібліотеки. Відносне ім'я файлу, що містить директорію, вкаже PHP підвантажити модуль щодо поточної директорії.

\-ini |

Показує імена конфігураційних файлів та відскановані каталоги.

**Приклад #6 Приклад `--ini`**

$ php --ini Configuration File (php.ini) Path: /usr/dev/php/5.2/lib Loaded Configuration File: /usr/dev/php/5.2/lib/php.ini Scan for additional .ini files in: (none) Additional .ini files parsed: (none)

\-rf | -rfunction |

Показує інформацію про вказану функцію або метод класу (наприклад, кількість та назви параметрів).

Ця опція доступна лише в тому випадку, якщо PHP був скомпільований з підтримкою [Reflection](book.reflection.md)

**Приклад #7 Базове використання `--rf`**

$ php --rf vardump Function public function vardump

-   Parameters { Parameter #0 $var Parameter #1 .

\-RC | -rclass |

Показує інформацію про вказаний клас (список констант, властивостей та методів).

Ця опція доступна лише в тому випадку, якщо PHP був скомпільований з підтримкою [Reflection](book.reflection.md)

**Приклад #8 Приклад `--rc`**

$ php --rc Directory Class [internal:standard](internal:standard) class Directory

-   Constants
    
-   Static properties
    
-   Static methods
    
-   Properties
    
-   Methods { Method public method close
    
    Method public method rewind
    
    Method public method read
    

\-re | -Rextension |

Показує інформацію про вказаний модуль (список опцій php.ini, певних функцій, констант і класів).

Ця опція доступна лише в тому випадку, якщо PHP був скомпільований з підтримкою [Reflection](book.reflection.md)

**Приклад #9 Приклад `--re`**

$ php --re json Extension extension #19 json version 1.2.1

-   Functions { Function function jsonencode { } Function function jsondecode

\-rz | -rzendextension |

Показує інформацію про конфігурацію зазначеного Zend-модуля (та сама інформація, яка повертається [phpinfo()](function.phpinfo.md)

\-ri | -rextinfo |

Показує інформацію про конфігурацію зазначеного модуля (та сама інформація, яка повертається [phpinfo()](function.phpinfo.md)). Конфігурацію ядра можна дізнатися, вказавши як ім'я модуля значення "main".

**Приклад #10 `--ri`**

$ php --ri date

date

date/time support => enabled "Olson" Timezone Database Version => 2009.20 Timezone Database => internal Default timezone => Europe/Oslo

Directive => Local Value => Master Value date.timezone => Europe/Oslo => Europe/Oslo date.defaultlatitude => 59.930972 => 59.930972 date.defaultlongitude => 10.776699 => 10.776699 date.sunsetzenith => 90.583333 => 90.583333 date.sunrisezenith => 90.583333 => 90.583333

> **Зауваження**
> 
> Опції `-rBRFEH` `--ini` і `--r[fcezi]` доступні лише у CLI.