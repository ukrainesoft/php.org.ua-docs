---
navigation:
  - regexp.reference.unicode.md: « Властивості Unicode-символів
  - regexp.reference.dot.md: Метасимвол крапка »
  - index.md: PHP Manual
  - reference.pcre.pattern.syntax.md: Опис синтаксису Perl-сумісних регулярних виразів
title: Якоря
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Якоря

За умовчанням, поза символьним класом метасимвол початку рядка (`^`) відповідає початку оброблюваних даних (якщо не використовуються модифікатори). Усередині символьного класу він (`^`) має зовсім інше значення.

Метасимвол початку рядка (`^`) не повинен бути першим символом шаблону Якщо у шаблоні використовуються кілька альтернатив, але повинен бути першим символом у кожній з альтернатив, в якій він зустрічається, якщо шаблон коли-небудь зіставний з відповідною гілкою. Якщо всі альтернативи починаються з метасимволу початку рядка (`^`), то шаблон обмежений для збігу виключно на початку рядка, кажуть, що шаблон «заякорений». (Існують й інші способи «заякорити» шаблон).

Відповідність метасимволу кінця рядка (знак долара, `$`) досягається тільки в кінці рядка або безпосередньо перед останнім символом у разі, якщо ним є переклад рядка (якщо модифікатори не вказані). Метасимвол кінця рядка (`$`) не повинен бути останнім символом шаблону Якщо використовується кілька альтернатив, але має бути останнім символом у кожній альтернативі, в якій він фігурує. Усередині символьного класу символ "$" не має спеціального значення.

Поведінка метасимволу кінця рядка може бути змінена модифікатором [PCRE\_DOLLAR\_ENDONLY](reference.pcre.pattern.modifiers.md) так, щоб він відповідав виключно кінцю рядка. Цей прапор не стосується спеціальної послідовності. \\Z.

Значення метасимволів початку та кінця рядка змінюється Якщо використовується модифікатор [PCRE\_MULTILINE](reference.pcre.pattern.modifiers.md). У цій ситуації, крім збігів на початку або в кінці рядка, метасимволи «^» та «$» відповідають позиції безпосередньо після символу перекладу рядка «\\n». Наприклад, шаблон /^abc$/ зустрічається у рядку «def\\nabc» у багаторядковому режимі і не зустрічається у нормальному режимі. Таким чином, шаблон який «заякорений» в однорядковому режимі, всі гілки якого, починаються з «^», не буде «заякореним» у багаторядковому режимі. Модифікатор [PCRE\_DOLLAR\_ENDONLY](reference.pcre.pattern.modifiers.md)игнорируется Если модификатор установлен[PCRE\_MULTILINE](reference.pcre.pattern.modifiers.md)

Слід зазначити, що службові послідовності \\A,\\Z и\\z можна використовувати зіставлення з початком чи кінцем рядка обох режимах. І якщо всі гілки шаблону починаються з \\A, шаблон будет «заякорен» независимо от присутствия модификатора[PCRE\_MULTILINE](reference.pcre.pattern.modifiers.md)
