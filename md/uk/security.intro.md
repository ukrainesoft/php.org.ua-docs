---
navigation:
  - security.md: « Безпека
  - security.general.md: Загальні міркування »
  - index.md: PHP Manual
  - security.md: Безпека
title: Вступ
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Вступ

PHP є потужною мовою програмування та інтерпретатором, що взаємодіє з веб-сервером як модуль або як незалежний бінарний CGI додаток. PHP здатний звертатися до файлів, виконувати різні команди на сервері та відкривати мережеві з'єднання. Саме тому всі скрипти, які виконуються на сервері, є потенційно небезпечними. PHP спочатку розроблялася як більш захищена (щодо Perl, C) мова для написання CGI-додатків. За допомогою ряду налаштувань під час компіляції, а також динамічних налаштувань програми ви завжди зможете знайти відповідне поєднання свободи дій і безпеки.

Оскільки існує багато різних способів використання PHP, є і безліч опцій, які керують його поведінкою. Широкий вибір опцій гарантує вам можливість використовувати PHP з різною метою, але також означає, що деякі комбінації опцій роблять сервер незахищеним.

Гнучкість конфігурування PHP можна порівняти з гнучкістю мови. PHP можна використовувати для створення повноцінних серверних додатків, що використовують доступні для вказаного користувача можливості операційної системи, або як прості файли, що підключаються, що зберігаються на сервері з мінімальним ризиком в жорстко контрольованому середовищі. Те, як налаштовано дане оточення, а також якість його безпеки, здебільшого залежить від PHP-розробника.

Цей розділ починається з розгляду деяких загальних питань безпеки, різних конфігураційних опцій та їх комбінацій, а також ситуацій, коли їх використання є безпечним. Крім того, наводяться деякі міркування щодо безпечного кодування.
