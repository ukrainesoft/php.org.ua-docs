---
navigation:
  - reference.pcre.pattern.modifiers.md: >-
      « Описує можливі модифікатори шаблонів Perl-сумісних регулярних виразів
      (PCRE)
  - ref.pcre.md: Функції PCRE »
  - index.md: PHP Manual
  - pcre.pattern.md: Регулярні вирази PCRE
title: Відмінності від Perl
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Відмінності від Perl

Наведені тут відмінності відносяться до версії Perl 5.005.

1.  За промовчанням пробіловий символ - це будь-який символ, який функція isspace() з бібліотеки C упізнає таким, хоча можливо скомпілювати PCRE з альтернативними таблицями символів. Функція isspace() визначає як пробіловий такі символи: пробіл, кінець сторінки (formfeed), переклад рядка, повернення каретки, горизонтальну табуляцію та вертикальну табуляцію. Perl 5 не включає вертикальну табуляцію в список пробілових символів. Екранування\\v Perl, що тривалий час був присутній у документації, насправді ніколи не розпізнавалася. Однак, символ як такий, вважався за пробільний до версії 5002. У 5.004 та 5.005 він не визначається як\\s.
2.  PCRE не дозволяє використовувати квантифікатори повторення в випереджальних припущеннях. Perl дозволяє, але вони не означають, про що ви могли подумати. Наприклад, (?! a) {3} не перевіряє, що наступні три символи не "a". Перевіряється лише те, що наступний символ не тричі.
3.  Захоплюючі підшаблони, які виникають у негативних випереджальних перевірках, вважаються, але їх записи у векторі зсувів ніколи не встановлюються. Perl встановлює числові змінні з будь-яких подібних масок, які збіглися до моменту, коли припущення не підтвердилося під час перевірки чогось, але тільки якщо випереджаюче припущення містить лише одну гілка.
4.  Хоча бінарні нульові символи підтримуються в рядку, що перевіряється, вони неприпустимі в рядку шаблону, тому що вона передається як нормальна C-рядок, в якій цей символ позначає кінець рядка. Для його використання в рядку шаблону необхідно скористатися конструкцією "\\x00".
5.  Наступні екрануючі послідовності Perl не підтримуються:\\l,\\u,\\L,\\U. Фактично вони реалізовані стандартним обробником рядків Perl і є частиною модуля обробки регулярних виразів.
6.  Припущення\\G з Perl також не підтримується, оскільки не має відношення до окремо взятої схеми збігів.
7.  Очевидно, що PCRE не підтримує конструкції (?{code}) і (??{code}). Проте є підтримка рекурсивних шаблонів.
8.  Є ще дивний момент при Perl 5.005\_02, пов'язаний із встановленням захоплених рядків, коли частина шаблону повторюється. Наприклад, перевірка "aba" шаблоном /^(a(b)?)+$/, встановлює $2 значення "b", але перевірка "aabbaa" шаблоном /^(aa(bb)?)+$/, залишає $2 не виставленою. Хоча, якщо шаблон поміняти на /^(aa(b(b))?)+$/, $2 (і $3) будуть встановлені. У Perl 5.004, $2 встановиться в обох випадках, і це також істинно для PCRE. Якщо в майбутньому Perl якось зафіксує цю поведінку, PRCE буде слідувати йому.
9.  Інша досі невирішена суперечність у тому, що Perl 5.005\_02, шаблоном /^(a)?(?(1)a|b)+$/ розпізнає рядок "a", а PCRE немає. Хоча і в Perl і PCRE, /^(a)?a/ розпізнає "a" і залишає $1 не виставленої.
10.  PCRE надає деякі розширення регулярних виразів Perl:

```
1.  Несмотря на то, что опережающие предположения должны распознавать строки фиксированной длины, каждое альтернативное ретроспективное предположение может распознавать строки разной длины. Perl 5.005 требует, чтобы они были одной длины.
2.  Если установлена [PCRE\_DOLLAR\_ENDONLY](reference.pcre.pattern.modifiers.md) и не установлена [PCRE\_MULTILINE](reference.pcre.pattern.modifiers.md), метасимвол $ распознается только в самом конце строки.
3.  Если установлена [PCRE\_EXTRA](reference.pcre.pattern.modifiers.md), обратный слеш с последующей за ним буквой, не имеющий специального значения, приводит к ошибке.
4.  Если установлена [PCRE\_UNGREEDY](reference.pcre.pattern.modifiers.md), жадность квантификаторов повторения инвертирована. То есть по умолчанию они не жадные, пока за ними не будет знак вопроса.
```
