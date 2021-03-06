- [«Символьні класи](regexp.reference.character-classes.md)
- [Встановлення внутрішніх опцій »](regexp.reference.internal-options.md)

- [PHP Manual](index.md)
- [Опис синтаксису Perl-сумісних регулярних виразів](reference.pcre.pattern.syntax.md)
- Альтернативний вибір

## Альтернативний вибір

Символ вертикальної межі '\|' використовується для поділу
альтернативних масок. Наприклад, шаблон 'gilbert|sullivan' відповідає
як "gilbert", і "sullivan". Допустимо вказувати будь-яку кількість
альтернатив, також можна вказувати порожні альтернативи
(відповідають порожньому рядку). У процесі пошуку відповідності
проглядаються всі перелічені альтернативи зліва направо,
зупиняючись після першої знайденої відповідності. У разі якщо
альтернативні варіанти перераховані в підмаску, весь шаблон збігається
лише у разі відповідності одного з альтернативних варіантів підмаски
та залишку основного шаблону.
