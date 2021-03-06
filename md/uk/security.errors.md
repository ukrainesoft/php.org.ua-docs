- [«SQL-ін'єкції](security.database.sql-injection.md)
- [Дані, введені користувачем »](security.variables.md)

- [PHP Manual](index.md)
- [Безпека](security.md)
- Повідомлення про помилки

# Повідомлення про помилки

З погляду безпеки висновок повідомлень про помилки несе як
плюси, і мінуси.

Одна із стандартних методик, які застосовуються в атаках - введення некоректних
даних з подальшим аналізом змісту та характеру повідомлень про
помилки. Це дає зломщику можливість перевірити скрипти та дані
сервера на наявність потенційних дірок. Наприклад, якщо зломщик отримав
деяку інформацію про сторінку на підставі відправки форми, він
спробує визначити деякі передані значення або
модифікувати їх:

**Приклад #1 Атака на змінні в HTML-сторінці**

```htmlcode
<form method="post" action="attacktarget?username=badfoo&password=badfoo">
<input type="hidden" name="username" value="badfoo" />
<input type="hidden" name="password" value="badfoo" />
</form>
````

Помилки, що виникають під час роботи скриптів, є досить цінною.
інформацією для розробника, що містить такі дані, як функція або
файл, а також номер рядка, в якому виникла помилка. Вся ця
інформація може бути використана для злому. Для PHP-розробника
досить звично користуватися такими функціями, як
[show_source()](function.show-source.md),
[highlight_string()](function.highlight-string.md) або
[highlight_file()](function.highlight-file.md) з метою налагодження, але на
працюючих сайтах це може відкрити інформацію про приховані змінні,
неперевіреному синтаксисі та інших потенційно небезпечних моментах.
Особливо небезпечно наявність коду з вбудованим механізмом налагодження
публічні частини сайту. Зломщик може спробувати запустити налагоджувальний
механізм, підбираючи основні ознаки налагодження:

**Приклад #2 Використання стандартних змін налагодження**

```htmlcode
<form method="post" action="attacktarget?errors=Y&showerrors=1&debug=1">
<input type="hidden" name="errors" value="Y" />
<input type="hidden" name="showerrors" value="1" />
<input type="hidden" name="debug" value="1" />
</form>
````

Незалежно від методу обробки помилок можливість перевірки системи на
наявність помилок забезпечує зломщика додатковою інформацією.

Наприклад, стандартний висновок про помилку вказує операційну систему,
якою виконуються PHP-скрипти. Якщо зломщик аналізує звичайну
сторінку сайту з розширенням .md та намагається дізнатися систему, за допомогою
якою працює сайт (для подальшого пошуку вразливих місць), то подаючи
на введення невірних даних він може виявити, що система використовує PHP.

Також повідомлення про помилку може дати інформацію про базу, що використовується
даних, або, наприклад, як побудовано логіку роботи скриптів. Це в
свою чергу, може дозволити зломщику підключитися до відкритого порту
бази даних, або визначити певні помилки в коді. Пробуючи по черзі
різні невірні блоки даних, зловмисник може визначити порядок
автентифікації у скрипті (наприклад, за номерами рядків з помилками) або
перевіряти на наявність дірок різні ділянки коду.

Виведення стандартних помилок або помилок, пов'язаних із файловою системою,
може вказати, з якими привілеями запущено веб-сервер, і як
організовано каталоги сайту. Обробка подібних помилок, написана
розробниками програми, може тільки погіршити проблему, якщо
зломщиком буде знайдено спосіб виявити "приховану" налагоджувальну
інформацію.

Існує три основні способи вирішення цієї проблеми. Перший
полягає в тому, щоб структурувати всі функції та спробувати
компенсувати обсяг помилок, що видаються. Другий спосіб – повністю
відключити у діючому коді виведення повідомлень про помилки. І наостанок,
третій спосіб – використовувати спеціальні засоби PHP для створення
власного обробника помилок. Залежно від використовуваної вами
політики безпеки ви можете застосувати у вашій конкретній ситуації
усі три способи.

Один з можливих способів убезпечити ваш код перед його публікацією в
загальний доступ – це використання функції PHP
[error_reporting()](function.error-reporting.md), яка може допомогти
виявити потенційно небезпечні змінні. Тестуючи код перед випуском
релізу за допомогою значення **`E_ALL`**, ви досить легко можете
виявити ділянки коду, у яких змінні може бути підмінені чи
модифіковані. Після закінчення тестування, ви можете або повністю
вимкнути всі повідомлення про помилки встановивши
[error_reporting()](function.error-reporting.md) в 0, або відключити
їх виведення за допомогою директиви `php.ini` `display_errors`, ізолювавши
таким чином ваш код від промацування. Якщо ви вирішили використати
останній спосіб, необхідно також вказати шлях до лог-файлу за допомогою
директиви `error_log` та включити директиву `log_errors`.

**Приклад #3 Пошук потенційно небезпечних змінних за допомогою E_ALL**

` <?phpif ($username) {  // Переменная не инициализируется или не проверяется перед использованием    $good_login = 1;}if ($good_login == 1) { // Если предыдущая проверка потерпела неудачу, переменная оказывается неинициализированной    readfile ("/highly /sensitive/data/index.md");}?> `
