- [« Коментарі](regexp.reference.comments.md)
- [Продуктивність »](regexp.reference.performance.md)

- [PHP Manual](index.md)
- [Опис синтаксису Perl-сумісних регулярних виразів](reference.pcre.pattern.syntax.md)
- Рекурсивні шаблони

## Рекурсивні шаблони

Розглянемо задачу пошуку відповідності з рядком, що знаходяться всередині
необмеженої кількості круглих дужок. Без використання рекурсії
найкраще, що можна зробити - написати шаблон, який вирішуватиме завдання
для деякої обмеженої глибини вкладеності, тому що обробити
необмежену глибину неможливо. У Perl 5.6
надано деякі експериментальні можливості, які в тому
числа дозволяють реалізувати рекурсію у шаблонах. Спеціальне позначення
(R) використовується для вказівки рекурсивної підмаски. Таким чином,
наведемо PCRE шаблон, що вирішує поставлене завдання (маю на увазі, що
використовується модифікатор
[PCRE_EXTENDED](reference.pcre.pattern.modifiers.md), незначні
пробіли ігноруються): `\( ( (?>[^()]+) | (?R) )* \)`

Спочатку він відповідає круглій дужці, що відкриває. Далі він
відповідає будь-якій кількості підрядків, кожна з яких може бути
послідовністю не-дужок, або рядком, що рекурсивно відповідає
шаблону (тобто рядком, коректно укладеним у круглі дужки). І, в
Нарешті, йде закриває кругла дужка.

Наведений приклад шаблону використовує вкладені необмежені
повторення, тому використання одноразових шаблонів значно
прискорює процес зіставлення, особливо у випадках, коли рядок не
відповідає заданій масці. Наприклад, якщо його застосувати до рядка:
`(aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa()`, то
невідповідність буде виявлено досить швидко. Але у випадку, якщо
одноразові шаблони не використовуються, зіставлення затягуватиметься на
тривалий час, оскільки існує безліч способів поділу
рядки між квантифікаторами + та \*, і всі вони мають бути перевірені,
перш ніж буде видано повідомлення про невдачу.

Значення, яке встановлюється для захоплюючої підмаски буде
відповідати значенню, захопленому на найглибшому рівні
рекурсії. У випадку, якщо наведений вище шаблон зіставляється з
рядком `(ab(cd)ef)`, захопленим значенням буде 'ef', яке є
останнім значенням, що приймається на верхньому рівні. У разі якщо
додати додаткові дужки `\( ( ( (?>[^()]+) | (?R) )* ) \)`,
захопленим значенням буде "ab(cd)ef". У випадку, якщо у шаблоні
зустрічається більш ніж 15 захоплюючих дужок, PCRE потрібно більше
пам'яті обробки рекурсії, ніж зазвичай. Пам'ять виділяється за допомогою
функції pcre_malloc, та звільняється відповідно функцією pcre_free.
Якщо пам'ять може бути виділено, зберігаються дані лише перших
15 захоплюючих дужок, тому що немає способу видати помилку out-of-memory
зсередини рекурсії.

`(?1)`, `(?2)` і так далі можуть бути використані для рекурсивних
підмасок. Також можна використовувати іменовані підмаски: `(?P>name)`
або `(?&name)`.

Якщо синтаксис посилання на рекурсивну підмаску (як на ім'я, так і на
числовому індексу) використовується поза дужками, до яких він належить, він
відпрацьовує аналогічно підпрограмі у мові програмування. Візьмемо
більш ранній приклад, що вказує, що шаблон
`(sens|respons)e and ibility` відповідає "sense and sensibility" та
"response and responsibility", але не "sense and responsibility". Якщо
замість цього використовувати шаблон `(sens|respons)e and (?1)ibility`, він
збігається з "sense and responsibility" так само, як і з іншими двома
рядками. Однак, такі посилання повинні бути вказані після підмаски,
яку вони посилаються.

Максимальний рядок рядка, що обробляється, не повинен перевищувати
максимально доступного цілого числа. Однак, так як для обробки
підмасок і нескінченного повторення PCRE використовує рекурсію, це
означає, що розмір рядків, що обробляються, в деяких шаблонах також
може бути обмежений доступним розміром стека.
