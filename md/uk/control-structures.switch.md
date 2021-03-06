- [«continue](control-structures.continue.md)
- [match »](control-structures.match.md)

- [PHP Manual](index.md)
- [Керування конструкції](language.control-structures.md)
- switch

## switch

(PHP 4, PHP 5, PHP 7, PHP 8)

Оператор switch схожий на ряд операторів IF з однаковою умовою. Во
багатьох випадках вам може знадобитися порівнювати одну й ту саму змінну
(або вираз) з безліччю різних значень і виконувати різні
ділянки коду в залежності від того, яке значення набуває ця
змінна (або вираз). Це саме той випадок, для якого зручний
оператор `switch`.

> **Примітка**: Зверніть увагу, що на відміну від деяких інших
> мов, оператор [continue](control-structures.continue.md)
> застосовується в конструкціях `switch` і діє подібно до оператора
> `break`. Якщо у вас конструкція `switch` знаходиться усередині циклу, і вам
> необхідно перейти до наступної ітерації циклу, використовуйте
> `continue 2`.

> **Примітка**:
>
> Зауважте, що конструкція switch/case використовує [не суворе порівняння
> (==)](types.comparisons.md#types.comparisions-loose).

Наступні два приклади ілюструють два різні способи написати те ж саме
саме. Один використовує ряд операторів `if` та `elseif`, а інший -
оператор `switch`:

**Приклад #1 Оператор `switch`**

`<?phpif ($i == 0) {    echo "i рівно 0";} elseif ($i == 1) {   echo "i рівно 1";} elseif   2";}switch ($i) {    case 0:        echo "i рівно 0"; break; case 1:        echo "i рівно 1"; break; case 2:        echo "i рівно 2"; break;}?> `

**Приклад #2 Оператор `switch` допускає порівняння з типом string**

`<?phpswitch ($i) {   case "яблуко":        echo "i це яблуко"; break; case "шоколадка":        echo "i це шоколадка"; break; case "пиріг":        echo "i це пиріг"; break;}?> `

Важливо зрозуміти, як оператор `switch` виконується, щоб уникнути помилок.
Оператор `switch` виконує рядок за рядком (насправді вираз
за виразом). Спочатку ніякий код не виконується. Тільки у випадку
знаходження оператора `case`, значення якого збігається зі значенням
вирази в операторі `switch`, PHP починає виконувати оператори. PHP
продовжує виконувати оператори до кінця блоку `switch` або доти,
доки не зустріне оператор `break`. Якщо ви не напишете оператор `break`
в кінці секції case, PHP продовжуватиме виконувати команди наступної
секції case. Наприклад:

`<?phpswitch ($i) {    case 0:        echo "i рівно 0"; case 1:        echo "i рівно 1"; case 2:        echo "i рівно 2";}?> `

У цьому прикладі, якщо $i дорівнює 0, то PHP виконає всі оператори echo!
Якщо $i дорівнює 1, PHP виконає два останні оператори echo. Ви
отримайте очікувану поведінку оператора ('i і 2' буде відображено)
тільки, якщо `$i` дорівнюватиме 2. Таким чином, важливо не забувати про
операторів `break` (навіть якщо ви, можливо, хочете уникнути його
використання за призначенням за певних обставин).

В операторі `switch` вираз обчислюється один раз і цей результат
порівнюється з кожним оператором case. У виразі `elseif`, вираз
обчислюється знову. Якщо ваша умова складніша, ніж проста
порівняння та/або знаходиться в циклі, конструкція `switch` може працювати
швидше.

Список операторів для виконання в секції case також може бути порожнім,
що просто передає управління списку операторів у наступній секції
case.

` <?phpswitch ($i) {   case 0:   case 1:   case 2:       echo "i менше чем 3, но break; case 3:        echo "i рівно 3";}?> `

Спеціальний вид конструкції case – `default`. Сюди керування потрапляє
тоді, коли не спрацював жоден із інших операторів case. Наприклад:

`<?phpswitch ($i) {    case 0:        echo "i рівно 0"; break; case 1:        echo "i рівно 1"; break; case 2:        echo "i рівно 2"; break; default:       echo "i не рівно 0, 1 або 2";}?> `

> **Примітка**: Декілька вказівок default викликають помилку
> **`E_COMPILE_ERROR`**.

Можливий альтернативний синтаксис для керуючої структури switch. Для
докладнішу інформацію дивіться [Альтернативний синтаксис для керуючих структур](control-structures.alternative-syntax.md).

`<?phpswitch ($i):   case 0:        echo "і рівно 0"; break; case 1:        echo "i рівно 1"; break; case 2:        echo "i рівно 2"; break; default:        echo "i не рівно 0, 1 або 2";endswitch;?> `

Можливе використання точки з комою замість двокрапки після оператора
case. Наприклад :

`<?phpswitch($beer){  case 'tuborg'; case 'carlsberg'; case 'heineken'; echo 'Добрий вибір'; break; default; echo 'Будь ласка, зробіть новий вибір...'; break;}?> `
