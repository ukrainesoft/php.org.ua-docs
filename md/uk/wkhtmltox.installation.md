---
navigation:
  - wkhtmltox.requirements.md: « Вимоги
  - wkhtmltox.configuration.md: Налаштування під час виконання »
  - index.md: PHP Manual
  - wkhtmltox.setup.md: Встановлення та налаштування
title: Установка
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Установка

Вихідний код цього модуля та двійкові файли для Windows доступні [» github](https://github.com/krakjoe/wkhtmltox),

Отримання вихідного коду та складання модуля:

```
git clone https://github.com/krakjoe/wkhtmltox
cd wkhtmltox
phpize
./configure --with-wkhtmltox=/path/to/wkhtmltox/installation
make
sudo make install
```

Отримання оновлень та повторне складання модуля:

```
cd wkhtmltox
phpize --clean
git pull origin master
phpize
./configure --with-wkhtmltox=/path/to/wkhtmltox/installation
make
sudo make install
```
