Встановлення

-   [« Требования](wkhtmltox.requirements.html)
    
-   [Настройка во время выполнения »](wkhtmltox.configuration.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](wkhtmltox.setup.html)
    
-   Встановлення
    

## Встановлення

Вихідний код цього модуля та двійкові файли для Windows доступні [» github](https://github.com/krakjoe/wkhtmltox)

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