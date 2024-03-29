---
navigation:
  - ds.requirements.md: « Вимоги
  - ds.constants.md: Обумовлені константи »
  - index.md: PHP Manual
  - ds.setup.md: Встановлення та налаштування
title: Установка
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Установка

Найпростіший спосіб встановлення через [» PECL](https://pecl.php.net/package/ds)

```
pecl install ds
```

Також ви можете самостійно зібрати його із вихідних джерел:

```
# Зависимости, которые, возможно, придётся установить
# sudo apt-get install git build-essential php7.0-dev

git clone https://github.com/php-ds/extension "php-ds"
cd php-ds

# Сборка и установка модуля
phpize
./configure
make
make install

# Очистка оставшихся артефактов
make clean
phpize --clean
```

Якщо ви використовуєте Windows, ви можете завантажити [» готову бібліотеку .dll з PECL](https://pecl.php.net/package/ds)

> **Зауваження** :
> 
> Якщо ви використовуєте Composer, рекомендується включити [» php-ds/php-ds](https://packagist.org/packages/php-ds/php-ds) у ваш проект, щоб ваш код залишався робочим, без того, встановлено модуль чи ні.
