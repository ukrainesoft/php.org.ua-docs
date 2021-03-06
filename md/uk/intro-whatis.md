- [«Вступ](introduction.md)
- [Можливості PHP »](intro-whatcando.md)

- [PHP Manual](index.md)
- [Вступ](introduction.md)
- Що таке PHP?

## Що таке PHP?

PHP (рекурсивний акронім словосполучення `PHP: Hypertext Preprocessor`) -
це поширена мова програмування загального призначення з відкритим
вихідним кодом. PHP спеціально сконструйований для веб-розробок та його
код може впроваджуватися безпосередньо у HTML.

Проста відповідь, але що вона може означати? Ось приклад коду:

**Приклад #1 Приклад програмування на PHP**

`<!DOCTYPE html><html>   <head>        <title>Приклад</title>    </head>    <body>         <?php | ?>    </body></html>`

Замість рутинного виведення HTML-коду командами мови (як це відбувається,
наприклад, в Perl або C), скрипт PHP містить HTML із вбудованим кодом (у
нашому випадку, це висновок тексту "Привіт, я – скрипт PHP!"). Код PHP
відокремлюється спеціальними [початковим та кінцевим тегами `<?php` і `?>`](language.basic-syntax.phpmode.md), які дозволяють
"перемикатися" на "PHP-режим" і виходити з нього.

PHP відрізняється від JavaScript тим, що PHP-скрипти виконуються на сервері
і генерують HTML, який надсилається клієнту. Якби у вас на сервері
був розміщений скрипт, подібний до вищенаведеного, клієнт отримав би тільки
результат його виконання, але не зміг би з'ясувати, який саме його код
зробив. Ви навіть можете налаштувати свій сервер таким чином, щоб
звичайні HTML-файли оброблялися PHP процесором, так що клієнти навіть
не зможуть дізнатися, чи отримують вони звичайний HTML-файл чи результат
виконання скрипту.

PHP вкрай простий для освоєння, але водночас здатний задовольнити
запити професійних програмістів Не лякайтеся довгого списку
можливостей PHP. Ви можете швидко почати, і вже протягом кількох
годин зможете створювати прості PHP-скрипти.

Хоча PHP, головним чином, призначений для роботи в середовищі веб-серверів,
область його застосування не обмежується лише цим. Читайте далі
не пропустіть розділ [Можливості PHP](intro-whatcando.md) або,
почніть безпосередньо з [Вступного посібника](tutorial.md), якщо
Вас цікавить виключно веб-програмування.
