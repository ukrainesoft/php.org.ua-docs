---
navigation:
  - faq.using.md: « Використання PHP
  - faq.md.md: PHP та HTML »
  - index.md: PHP Manual
  - faq.md: ЧАВО
title: Безпечне хешування паролів
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Безпечне хешування паролів

У цьому розділі пояснюються причини, що стоять за хешування паролів з метою безпеки, а також ефективні методи хешування.

1.  [Чому я повинен хешувати паролі користувачів у моїй програмі?](#faq.passwords.hashing)
2.  [Чому популярні функції хешування, такі як md5 і sha1 не підходять для паролів?](#faq.passwords.fasthash)
3.  [Якщо популярні функції, що хешують, не підходять, як же я тоді повинен хешувати свої паролі?](#faq.passwords.bestpractice)
4.  [Що таке сіль?](#faq.passwords.salt)
5.  [Як я маю зберігати свою сіль?](#faq.password.storing-salts)

**Чому я повинен хешувати паролі користувачів у моїй програмі?**

Хешування паролів є одним з найголовніших міркувань безпеки, які необхідно зробити при розробці програми, яка приймає паролі від користувачів. Без хешування паролі, що зберігаються в базі вашої програми, можуть бути вкрадені, наприклад, якщо ваша база даних була скомпрометована, а потім негайно можуть бути застосовані для компрометації не тільки вашої програми, але й облікових записів ваших користувачів на інших сервісах, якщо вони не використовують унікальні паролі.

Застосовуючи хешуючий алгоритм до паролів користувача перед збереженням їх у своїй базі даних, ви унеможливлюєте розгадування оригінального пароля для атакуючого вашу базу даних, в той же час зберігаючи можливість порівняння отриманого хешу з оригінальним паролем.

Важливо, однак, що хешування паролів захищає їх тільки від компрометування у вашому сховищі, але не обов'язково від втручання шкідливого коду у вашому додатку.

**Чому популярні функції хешування, такі як [md5()](function.md5.md) і [sha1()](function.sha1.md)не подходят для паролей?**

Такі хешуючі алгоритми як MD5, SHA1 та SHA256 були спроектовані дуже швидкими та ефективними. За наявності сучасних технологій та обладнання, стало досить просто з'ясувати результат цих алгоритмів методом "грубою сили" для визначення оригінальних даних, що вводяться.

Через ту швидкість, з якою сучасні комп'ютери можуть "звернути" ці хешуючі алгоритми, багато професіоналів комп'ютерної безпеки суворо не рекомендують використовувати їх для хешування паролів.

**Якщо популярні функції, що хешують, не підходять, як же я тоді повинен хешувати свої паролі?**

При хешуванні паролів існує два важливі міркування: це вартість обчислення та сіль. Що вартість обчислення хешируючого алгоритму, то більше часу потрібно для злому його виведення методом " грубої сили " .

PHP предоставляет[вбудоване API хешування паролів](book.password.md), яке безпечно працює і з [хешуванням](function.password-hash.md) і з [перевіркою паролів](function.password-verify.md)

Іншою можливістю є функція [crypt()](function.crypt.md)що підтримує кілька алгоритмів хешування. При використанні цієї функції ви можете бути впевненим, що вибраний вами алгоритм доступний, оскільки PHP містить власну реалізацію кожного алгоритму, що підтримується, навіть у випадку, якщо якісь з них не підтримуються вашою системою.

При хешуванні паролів рекомендується застосовувати алгоритм Blowfish, який також використовується за умовчанням в API хешування паролів, так як він значно більшої обчислювальної складності, ніж MD5 або SHA1, при цьому, як і раніше, є гнучким.

Врахуйте, що якщо ви використовуєте функцію [crypt()](function.crypt.md) Для перевірки пароля, то вам потрібно застерегти себе від атак за часом, застосовуючи порівняння рядків, що займає постійний час. Ні оператори PHP [\== і ===](language.operators.comparison.md), ни функция[strcmp()](function.strcmp.md) не є такими. Функція ж [password\_verify()](function.password-verify.md) робить те, що потрібно. Настійно рекомендується використовувати [вбудоване API хешування паролів](book.password.md)якщо є така можливість.

**Що таке сіль?**

Криптографічна сіль являє собою дані, які застосовуються в процесі хешування для запобігання можливості розгадати оригінальне введення за допомогою пошуку результату хешування в списку заздалегідь обчислених пар введення-хеш, відомому також як "райдужна" таблиця.

Простішими словами, сіль - це шматочок додаткових даних, які роблять ваші хеші набагато стійкішими до злому. Існує багато онлайн-сервісів, що надають великі списки заздалегідь обчислених хешей разом з їх оригінальним введенням. Використання солі робить пошук результуючого хешу у такому списку малоймовірним чи навіть неможливим.

[password\_hash()](function.password-hash.md) створює випадкову сіль у разі, якщо вона не була передана, і найчастіше це найкращий та безпечний вибір.

**Як я маю зберігати свою сіль?**

При использовании функции[password\_hash()](function.password-hash.md) або [crypt()](function.crypt.md), що повертається вже містить сіль як частина створеного хеша. Це значення потрібно зберігати як є у вашій базі даних, так як воно містить також інформацію про хешируючу функцію, яка використовувалася, і може бути безпосередньо передано до функцій [password\_verify()](function.password-verify.md) або [crypt()](function.crypt.md)при проверке пароля.

Наступна діаграма показує формат значення, що повертається функціями [crypt()](function.crypt.md) або [password\_hash()](function.password-hash.md). Як можна бачити, вони містять повну інформацію про алгоритм і солі, потрібні для майбутньої перевірки пароля.

![Компоненти значення, що повертаються функціями password_hash та crypt, йдуть у наступному порядку:
обраний алгоритм, опції алгоритму, сіль та хеш пароля.](images/2a34c7f2e658f6ae74f3869f2aa5886f-crypt-text-rendered.svg)
