- [«Повторення](regexp.reference.repetition.md)
- [Затвердження »](regexp.reference.assertions.md)

- [PHP Manual](index.md)
- [Опис синтаксису Perl-сумісних регулярних виразів](reference.pcre.pattern.syntax.md)
- Зворотні посилання

## Зворотні посилання

Поза символьним класом зворотний сліш з наступною цифрою більше нуля
(і, можливо, наступними цифрами) інтерпретується як посилання на
попередню захоплюючу підмаску, припускаючи, що відповідне
кількість попередніх відкривають круглих дужок є.

Однак, якщо наступне за зворотним слідом число менше 10, воно
завжди інтерпретується як зворотне посилання, і призводить до помилки тільки
у тому випадку, якщо немає відповідної кількості дужок, що відкривають.
Інакше кажучи, відкриваючі дужки нічого не винні передувати посиланні для
чисел менше 10. "Упереджувальне зворотне посилання" може мати сенс, якщо
використовується повторення і пізніша підмаска бере участь у ранній
ітерації. Дивіться розділ
[escape-послідовності](regexp.reference.escape.md) для отримання
додаткових відомостей про обробку цифр, що йдуть за зворотним слішем.

Зворотне посилання зіставляється з частиною рядка, захопленого
відповідною підмаскою, але не з самою підмаскою. Таким чином шаблон
`(sens|respons)e and ibility` відповідає "sense and sensibility",
"response and responsibility", але не "sense and responsibility". В
у випадку, якщо зворотне посилання виявлено під час реєстрозалежного
пошуку, то при зіставленні зворотного посилання регістр також враховується.
Наприклад, `((?i)rah)\s+ ` відповідає "rah rah" і "RAH RAH", але не
"RAH rah", хоча сама підмаска зіставляється без урахування регістру.

На ту саму підмаску може бути кілька посилань. Якщо підмаска не
брала участь у зіставленні, то зіставлення з посиланням на неї завжди
зазнає невдачі. Наприклад, шаблон `(a|(bc))` зазнає невдачі, якщо
знаходить відповідність з "a" раніше, ніж із "bc". Оскільки може бути до
99 зворотних посилань, всі цифри, що йдуть за зворотним слідком,
розглядаються як частина потенційного зворотного посилання. Якщо за посиланням
повинна слідувати цифра, необхідно використовувати обмежувач. В разі,
якщо вказано прапорець [PCRE_EXTENDED](reference.pcre.pattern.modifiers.md),
обмежувачем може бути будь-який пробільний символ. В іншому випадку
можна використовувати порожній коментар.

Посилання на підмаску, всередині якої вона розташована, завжди терпить
невдачу, якщо це перше зіставлення поточної підмаски. Наприклад,
шаблон (a ) відповідає жодному рядку. Але все ж такі посилання
бувають корисні в підмасках, що повторюються. Наприклад, шаблон `(a|b )+`
збігається з будь-якою кількістю "a", "aba", "ababaa"... При кожній
ітерації підмаски зворотне посилання відповідає частині рядка,
яка була захоплена за попередньої ітерації. Щоб така конструкція
працювала, шаблон має бути побудований так, щоб при першій ітерації
зіставлення зі зворотним посиланням не проводилося. Цього можна досягти,
використовуючи альтернативи (як у попередньому прикладі), або квантифікатори з
мінімумом, рівним нулю.

Керуюча послідовність `\g` може бути використана для
абсолютних та відносних посилань на підмаски. Після цієї
послідовності має бути вказано беззнакове або негативне
число, за бажання укладене у фігурні дужки. Послідовності
``, `\g1' і `\g{1}' еквівалентні один одному. Використання цього
шаблону з беззнаковим числом допоможе уникнути двозначності, властивої
числам після зворотного сліша. Це також допомагає відрізнити зворотні
посилання від символів у вісімковому форматі, а також спрощує запис
числового літералу відразу після зворотного посилання, наприклад, '\g{2}1'.

Використання негативних чисел з `\g` корисно при використанні
відносних посилань. Наприклад, `(foo)(bar)\g{-1}` відповідає
"foobarbar", а `(foo)(bar)\g{-2}` відповідає "foobarfoo". це також
може бути корисно в довгих шаблонах, як альтернатива
відстеження числа підмасок, на які можна посилатися у наступному
частин шаблону.

Вказати зворотне посилання на іменовану підмаску можна за допомогою
`(?P=name)`, `\k<name>`, `\k'name'`, `\k{name}`, `\g{name}`, `\g<name>`
або `\g'name'.
