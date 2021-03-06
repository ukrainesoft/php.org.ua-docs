- [« API для плагінів до вбудованого драйвера MySQL](mysqlnd.plugin.md)
- [Отримання API плагінів mysqlnd »](mysqlnd.plugin.obtaining.md)

- [PHP Manual](index.md)
- [API для плагінів до вбудованого драйвера MySQL](mysqlnd.plugin.md)
- Порівняння плагінів mysqlnd з MySQL Proxy

## Порівняння плагінів mysqlnd з MySQL Proxy

Плагіни `mysqlnd` та MySQL Proxy - це різні технології, що використовують
різні підходи. Обидва варіанти є підходящими інструментами для
вирішення різноманітних стандартних завдань, таких як балансування
навантаження, моніторинг та покращення продуктивності. Важливою відмінністю
є те, що MySQL Proxy працює з усіма клієнтами MySQL, тоді
як плагіни `mysqlnd` - лише для PHP-додатків.

Як модуль PHP, плагін `mysqlnd` встановлюється на сервері додатків
PHP разом з рештою PHP. MySQL Proxy може бути запущений на сервері
програм PHP або ж бути встановлений на окремій машині для підтримки
множинних серверів програм PHP.

Установка MySQL Proxy на сервері додатків має дві переваги:

1. Відсутність єдиної точки відмови

2. Легкість у масштабуванні (горизонтальному або клієнтському)

MySQL Proxy (а також плагіни `mysqlnd`) можуть легко вирішувати проблеми,
заради вирішення яких інакше знадобилися б зміни до існуючих
додатках.

Тим не менш, у MySQL Proxy є деякі недоліки:

- MySQL Proxy - це новий елемент та технологія, яку потрібно
вивчити та встановити

- MySQL Proxy вимагає знання скриптової мови Lua

MySQL Proxy може бути змінено за допомогою C та Lua. Lua є
кращою скриптовою мовою для MySQL Proxy. Для більшості
експертів PHP, Lua є новою мовою, яку треба вивчати. Плагін
`mysqlnd` може бути написаний на C. Також можна написати плагін на PHP,
використовуючи [»PECL/mysqlnd_uh](http://pecl.php.net/package/mysqlnd_uh).

MySQL Proxy працює як демон – фоновий процес. MySQL Proxy може
згадати раніше прийняті рішення, тому що весь стан може бути
збережено. Однак плагіни `mysqlnd` прив'язані до життєвого циклу PHP,
що базується на запитах. Також MySQL Proxy може розділяти один раз
отриманий результат між різними серверами програм. Плагіни
`mysqlnd` для вирішення цього завдання повинні використовувати якесь
постійне сховище для збереження результатів між запитами.
Наприклад, для цього може бути використаний інший демон, такий як
Memcache. Так що в цьому випадку MySQL Proxy працює явно краще.

MySQL Proxy працює поверх мережевих протоколів. За допомогою MySQL Proxy ви
можете розібрати та піддати інженерному аналізу протокол MySQL Client
Server. Що-небудь змінити можна лише маніпулюючи протоколом обміну.
Якщо протокол раптом зміниться (що трапляється вкрай рідко), скрипти
MySQL Proxy буде потрібно переписувати.

Плагіни `Mysqlnd` працюють поверх C API, який дублює клієнт
`libmysqlclient`. Це C API по суті звичайна обгортка навколо протоколу
MySQL Client Server. Ви можете перехоплювати всі дзвінки C API. PHP
використовує C API, фактично, ви можете перехоплювати взагалі всі виклики
PHP без необхідності програмувати на рівні протоколу обміну.

`Mysqlnd` реалізує протокол обміну. Таким чином, плагіни можуть
перехоплювати, досліджувати, міняти і навіть повністю замінювати протокол
зв'язку. Хоча зазвичай нічого цього не потрібне.

Плагіни дозволяють використовувати два рівня (C API і протокол обміну),
у цьому вони набагато гнучкіші, ніж MySQL Proxy. Якщо плагін `mysqlnd`
реалізований з використанням C API, зміни протоколу обміну
вимагатимуть зміни плагіну.
