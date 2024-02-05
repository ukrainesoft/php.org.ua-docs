---
navigation:
  - fann.requirements.md: « Вимоги
  - fann.configuration.md: Налаштування під час виконання »
  - index.md: PHP Manual
  - fann.setup.md: Встановлення та налаштування
title: Установка
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Установка

Модуль FANN має працювати на будь-яких дистрибутивах Linux.

-   [Встановлення бібліотеки FANN](fann.installation.md#fann.installation.lib)
-   [Установка з PECL](fann.installation.md#fann.installation.pecl)
-   [Ручне встановлення](fann.installation.md#fann.installation.manual)

## Встановлення бібліотеки FANN

Перед початком встановлення переконайтеся, що на вашій системі вже встановлена ​​бібліотека *libfann*. Вона є частиною головного репозиторію для більшості дистрибутивів Linux (шукайте за словом *fann*). Вам потрібна версія для розробників.

Якщо вона не встановлена, то вам все ж таки доведеться її встановити. Можете встановити її з репозиторію ОС чи завантажити з [» офіційного сайту](http://leenissen.dk/fann/wp/)Например для Fedora:

```
$ sudo yum install fann-devel
```

або Ubuntu:

```
$ sudo apt-get install libfann-dev
```

Якщо бібліотека встановлюється вручну, спочатку потрібно видалити стару версію бібліотеки, інакше вона не буде замінена.

## Установка з PECL

Цей модуль доступний у PECL. Установка дуже проста, запустіть:

```
$ sudo pecl install fann
```

## Ручне встановлення

Для розробників і людей, зацікавлених у найсвіжішій версії, є можливість скомпілювати з найсвіжіших вихідних кодів, які лежать на [» GitHub](https://github.com/bukka/php-fann). . Зайдіть на GitHub та натисніть "Download ZIP". після цього запустіть:

```
$ unzip php-fann-master.zip
$ cd php-fann-master
$ phpize
$ ./configure
$ make all
$ sudo make install
```

Внесіть такі зміни до php.ini:

-   Впевніться, що*extension\_dir*вказує на директорію, в якій знаходиться*fann.so*. При складанні на екран буде виведено, куди саме встановлюється скомпільований модуль:
    
    ```
    Installing '/usr/lib/php/extensions/no-debug-non-zts-20060613/fann.so'
    ```
    
    Переконайтеся, що це шлях, в якому лежать модулі PHP:
    
    ```
    $ php -i | grep extension_dir
      extension_dir => /usr/lib/php/extensions/no-debug-non-zts-20060613 =>
                       /usr/lib/php/extensions/no-debug-non-zts-20060613
    ```
    
    Якщо це не так, то поміняйте*extension\_dir*у php.ini або просто перемістіть*fann.so*куди слід.
    
-   Для завантаження модуля при запуску PHP додайте в php.ini рядок:
    
    ```
    extension=fann.so
    ```
