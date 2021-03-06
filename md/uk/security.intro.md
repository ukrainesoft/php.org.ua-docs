- [«Безпека](security.md)
- [Загальні міркування»](security.general.md)

- [PHP Manual](index.md)
- [Безпека](security.md)
- Вступ

# Вступ

PHP є потужною мовою програмування та інтерпретатором,
що взаємодіє з веб-сервером як модуль або як незалежне
бінарне CGI програму. PHP здатний звертатися до файлів, виконувати
різні команди на сервері та відкривати мережеві з'єднання. Саме
тому всі скрипти, що виконуються на сервері, є потенційно
небезпечними. PHP спочатку розроблявся як більш захищений
(щодо Perl, C) мова для написання програм CGI. За допомогою
ряду налаштувань під час компіляції, а також динамічних налаштувань
програми, ви завжди зможете знайти відповідне поєднання свободи
дій та безпеки.

Оскільки існує багато різних способів використання PHP, є
і безліч опцій, які керують його поведінкою. Широкий вибір опцій
гарантує вам можливість використовувати PHP у різних цілях, але також
означає, що деякі комбінації опцій роблять сервер незахищеним.

Гнучкість конфігурування PHP можна порівняти з гнучкістю мови.
PHP можна використовувати для створення повноцінних серверних програм,
які використовують доступні для вказаного користувача можливості
операційної системи, або в якості простих файлів, що підключаються,
що зберігаються на сервері з мінімальним ризиком у жорстко контрольованій
середовище. Те, як настроєне дане оточення, а також якість його
безпеки, переважно залежить від PHP-розробника.

Цей розділ починається з розгляду деяких загальних питань
безпеки, різних конфігураційних опцій та їх комбінацій, а також
ситуацій, коли їх використання є безпечним. Крім того,
наводяться деякі міркування щодо безпечного кодування.
