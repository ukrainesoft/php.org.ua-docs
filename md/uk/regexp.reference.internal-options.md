---
navigation:
  - regexp.reference.alternation.md: « Альтернативний вибір
  - regexp.reference.subpatterns.md: Підмаски »
  - index.md: PHP Manual
  - reference.pcre.pattern.syntax.md: Опис синтаксису Perl-сумісних регулярних виразів
title: Встановлення внутрішніх опцій
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Встановлення внутрішніх опцій

Установки[PCRE\_CASELESS](reference.pcre.pattern.modifiers.md) [PCRE\_MULTILINE](reference.pcre.pattern.modifiers.md) [PCRE\_DOTALL](reference.pcre.pattern.modifiers.md) [PCRE\_UNGREEDY](reference.pcre.pattern.modifiers.md) [PCRE\_EXTRA](reference.pcre.pattern.modifiers.md) [PCRE\_EXTENDED](reference.pcre.pattern.modifiers.md)и PCRE\_DUPNAMES можуть бути локально визначені в шаблоні з використанням спеціальних Perl-послідовностей між символами «(?» і «)». Нижче наведено список цих опцій:

<table class="doctable table"><caption><strong>Символи внутрішніх опцій</strong></caption><tbody class="tbody"><tr><td><code class="literal">i&lt; /code&gt;</code></td><td>для <a href="reference.pcre.pattern.modifiers.md" class="link">PCRE_CASELESS</a></td></tr><tr><td><code class="literal">m</code></td><td>для <a href="reference.pcre.pattern.modifiers.md" class="link">PCRE_MULTILINE</a></td></tr><tr><td><code class="literal">s</code></td><td>для <a href="reference.pcre.pattern.modifiers.md" class="link">PCRE_DOTALL</a></td></tr><tr><td><code class="literal">x</code></td><td>для <a href="reference .pcre.pattern.modifiers.md" class="link">PCRE_EXTENDED</a></td></tr><tr><td><code class="literal">U</code></td><td>для <a href="reference.pcre.pattern.modifiers.md" class="link">PCRE_UNGREEDY</a></td></tr><tr><td><code class=" literal">X</code></td><td>для <a href="reference.pcre.pattern.modifiers.md" class="link">PCRE_EXTRA</a> (більше не підтримується з PHP 7.3)</td></tr><tr><td><code class="literal">J</code></td><td>для <a href="reference.pcre.pattern.modifiers.md" class="link">PCRE_INFO_JCHANGED</a></td></tr></tbody></table>

Наприклад, (?im) вказує на реєстронезалежний, багаторядковий режим пошуку. Також можна скинути опцію, поставивши перед нею символ "-", або комбінувати установку та скасування режимів. Наприклад, (?im-sx) встановлює прапори [PCRE\_CASELESS](reference.pcre.pattern.modifiers.md) [PCRE\_MULTILINE](reference.pcre.pattern.modifiers.md) та скасовує прапори [PCRE\_DOTALL](reference.pcre.pattern.modifiers.md) і [PCRE\_EXTENDED](reference.pcre.pattern.modifiers.md). Якщо символ розташований одночасно після та перед символом «-», опцію буде скасовано.

Якщо зміна опції відбувається на самому верхньому рівні (тобто поза підмаскою), зміна буде застосована до частини шаблону, що залишилася. Таким чином, `/ab(?i)c/` збігається лише з «abc» та «abC».

Якщо зміна налаштування відбувається всередині підмаски, ефект буде іншим. Це зміна поведінки у Perl 5.005. Зміна опції всередині підмаски вплине тільки на частину цієї підмаски, що залишилася, тобто `(a(?i)b)c` збігається тільки з «abc» і «aBc» і більше ні з чим (зрозуміло, якщо [PCRE\_CASELESS](reference.pcre.pattern.modifiers.md) не увімкнуто). Це означає, що різні частини шаблону опції можуть відрізнятися. Будь-які зміни, що відбулися в одній альтернативній гілці, переносяться і в інші гілки в межах підмаски. Наприклад, `(a(?i)b|c)` збігається з "ab", "aB", "c", і "C", хоча і при збігу з "C" перша гілка була відкинута до установки опції. Це тому, що встановлення всіх опцій відбувається на етапі компіляції. В іншому випадку могла бути дуже дивна поведінка.

Опції, специфічні для PCRE, такі як [PCRE\_UNGREEDY](reference.pcre.pattern.modifiers.md) і [PCRE\_EXTRA](reference.pcre.pattern.modifiers.md) можуть бути встановлені так само, як і Perl-сумісні опції, шляхом використання символів U і X відповідно. Прапор (?X) специфічний тим, що повинен бути розташований у шаблоні, перш ніж використовувати будь-яку іншу додаткову можливість, навіть якщо він розташований на верхньому рівні. Найкраще розміщувати прапор (?X) на самому початку шаблону.
