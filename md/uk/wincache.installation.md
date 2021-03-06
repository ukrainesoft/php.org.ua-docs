- [« Вимоги](wincache.requirements.md)
- [Налаштування під час виконання »](wincache.configuration.md)

- [PHP Manual](index.md)
- [Встановлення та налаштування](wincache.setup.md)
- Установка

## Установка

Цей модуль [»PECL](https://pecl.php.net/) не поставляється разом з
PHP.

Інформація щодо встановлення цього модуля PECL може бути знайдена у розділі
керівництва [Встановлення модулів PECL](install.pecl.md). Додаткова
інформація, така як нові версії, завантаження, вихідні файли,
інформація про розробника та CHANGELOG, може бути знайдена тут:
[»https://pecl.php.net/package/wincache](https://pecl.php.net/package/wincache).

Існує два пакети для цього модуля: один пакет для PHP 5.2.X, а
інший для PHP 5.3.X. Вибір пакета залежить від вашої версії
PHP.

Для встановлення та увімкнення модуля виконайте наступні інструкції:

1. Розархівуйте пакет у тимчасову папку.

2. Скопіюйте `php_wincache.dll` у каталог із модулями PHP. Зазвичай цей
каталог називається "ext" і розташований там, де встановлений PHP. До
Наприклад: `C:\Program Files\PHP xt`.

3. Використовуючи текстовий редактор, відкрийте файл php.ini, який зазвичай
лежить там, де встановлено PHP. Наприклад:
`C:\Program Files\PHP\php.ini`.

4. Додайте до кінця файлу рядок: `extension = php_wincache.dll`.

5. Збережіть та закрийте файл `php.ini`.

6. Перестворіть пул додатків IIS для того, щоб зміни вступили до
силу. Щоб перевірити, чи модуль увімкнено, створіть файл
`phpinfo.php` з кодом, що викликає функцію PHP
[phpinfo](function.phpinfo.md).

7. Збережіть `phpinfo.php` у кореневому каталозі веб-сайту та зверніться до
ньому через веб-браузер за наступним посиланням
http://localhost/phpinfo.php. Знайдіть у виведенні секцію `wincache`.
Якщо модуль увімкнено, то функція [phpinfo](function.phpinfo.md)
покаже список параметрів конфігурації WinCache.

> **Примітка**: Не забудьте видалити файл `phpinfo.php` після того, як
> він перестане бути потрібним.
