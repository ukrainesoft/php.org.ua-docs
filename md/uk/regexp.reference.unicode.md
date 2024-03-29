---
navigation:
  - regexp.reference.escape.md: « Екрануючі послідовності
  - regexp.reference.anchors.md: Якоря »
  - index.md: PHP Manual
  - reference.pcre.pattern.syntax.md: Опис синтаксису Perl-сумісних регулярних виразів
title: Властивості Unicode-символів
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Властивості Unicode-символів

Починаючи з версії 5.1.0, були додані три додаткові послідовності, що управляють, збігаються з деякими загальними символьними типами *у режимі UTF-8*Вот они:

*\\p{xx}*

символ із властивістю xx

*\\P{xx}*

символ без якості xx

*\\X*

розширена послідовність Unicode

Імена властивостей, представлені вище як `xx`, обмежені загальними категоріями властивостей Unicode. Кожен символ має рівно одну таку властивість, що вказується дволітерною абревіатурою. Для сумісності з Perl також можна вказати заперечення додаванням знака «^» між дужкою та ім'ям властивості. Наприклад, `\p{^Lu}` — це те саме, що й `\P{Lu}`

Якщо з `\p`или`\P` вказана лише одна літера, вона включає всі властивості, що починаються з цієї літери. У разі, якщо не використовується заперечення, фігурні дужки необов'язкові; наступні два приклади еквівалентні:

```
\p{L}
\pL
```

**Підтримувані коди властивостей**

| Свойство | Совпадение | Замечание |
| --- | --- | --- |
| `C` | інше |  |
| `Cc` | Control |  |
| `Cf` | Формат |  |
| `Cn` | Не присвоєно |  |
| `Co` | Приватне використання |  |
| `Cs` | Сурогат |  |
| `L` | Літера | Включає такі властивості: `Ll` `Lm` `Lo` `Lt`и`Lu` |
| `Ll` | Рядкова літера |  |
| `Lm` | Модифікатор літери |  |
| `Lo` | Інша літера |  |
| `Lt` | велика буква |  |
| `Lu` | Прописна буква |  |
| `M` | Знак |  |
| `Mc` | Пробільний знак |  |
| `Me` | Навколишній знак |  |
| `Mn` | Не пробільний знак |  |
| `N` | Число |  |
| `Nd` | Десяткова кількість |  |
| `Nl` | Літерне число |  |
| `No` | Інше число |  |
| `P` | Пунктуація |  |
| `Pc` | З'єднувальна пунктуація |  |
| `Pd` | Знаки тире |  |
| `Pe` | Закриваюча пунктуація |  |
| `Pf` | Заключна пунктуація |  |
| `Pi` | Початкова пунктуація |  |
| `Po` | Інша пунктуація |  |
| `Ps` | Відкриваюча пунктуація |  |
| `S` | Символ |  |
| `Sc` | Грошовий знак |  |
| `Sk` | Модифікатор символу |  |
| `Sm` | Математичний символ |  |
| `So` | Інший символ |  |
| `Z` | Розділювач |  |
| `Zl` | Розділювач рядка |  |
| `Zp` | Розділювач абзацу |  |
| `Zs` | Пробільний роздільник |  |

Розширені властивості, такі як музичні символи (`InMusicalSymbols`) не підтримуються в PCRE.

Вказування реєстронезалежного (безреєстрового) режиму не впливає на ці керуючі послідовності. Наприклад, `\p{Lu}` завжди збігається тільки з великими літерами.

Підмножини Unicode символів описуються як такі, що належать певним сценаріям. Будь-який символ цих підмножин може бути знайдений з використанням імені сценарію. Наприклад:

-   `\p{Greek}`
-   `\P{Han}`

Також ті символи, які не є частиною конкретного сценарію об'єднані разом у сценарій `Common`Текущий список сценариев:

< td>`Kayah_Li`< /tr>< td>`Ugaritic`

<table class="doctable table"><caption><strong>Підтримувані сценарії</strong></caption><tbody class="tbody"><tr><td><code class="literal">Arabic</code></td><td><code class="literal">Armenian</code></td><td><code class="literal">Avestan</code></td><td>&lt; code class="literal"&gt;Balinese</td><td><code class="literal">Bamum</code></td></tr><tr><td><code class="literal">Batak</code></td><td><code class="literal">Bengali</code></td><td><code class="literal">Bopomofo</code>&lt; /td&gt;</td><td><code class="literal">Brahmi</code></td><td><code class="literal">Braille</code></td></tr><tr><td><code class="literal">Buginese</code></td><td><code class="literal">Buhid</code></td><td><code class="literal">Canadian_Aboriginal</code></td><td><code class="literal">Carian</code></td><td><code class="literal">Chakma</code></td></tr><tr><td><code class="literal">Cham</code></td><td><code class="literal">Cherokee</code></td><td><code class="literal">Common</code></td><td><code class="literal">Coptic</code></td><td><code class="literal">Cuneiform&lt; /code&gt;</code></td></tr><tr><td><code class="literal">Cypriot</code></td><td><code class="literal">Cyrillic</code></td><td><code class="literal">Deseret</code></td><td><code class="literal">Devanagari</code></td><td><code class="literal">Egyptian_Hieroglyphs</code></td></tr><tr><td><code class="literal">Ethiopic</code></td><td><code class="literal ">Georgian</code></td><td><code class="literal">Glagolitic</code></td><td><code class="literal">Gothic</code></td><td><code class="literal">Greek</code></td></tr><tr><td><code class="literal">Gujarati</code></td><td><code class="literal">Gurmukhi</code></td><td><code class="literal">Han</code></td><td><code class="literal">Hangul</code></td><td><code class="literal">Hanunoo</code></td></tr><tr><td><code class="literal">Hebrew</code></td><td><code class="literal">Hiragana</code></td><td><code class="literal">Imperial_Aramaic</code></td><td><code class="literal">Inherited</code></td><td><code class="literal">Inscriptional_Pahlavi</code></td></tr><tr><td><code class=" literal">Inscriptional_Parthian</code></td><td><code class="literal">Javanese</code></td><td><code class="literal">Kaithi</code></td><td><code class="literal">Kannada</code></td><td><code class="literal">Katakana</code></td></tr><tr><td><code class="literal">Kharoshthi</code></td><td><code class="literal">Khmer</code></td><td><code class="literal">Lao</code></td><td><code class="literal">Latin</code></td></tr><tr><td><code class="literal">Lepcha</code></td><td><code class="literal">Limbu</code></td><td>&lt; code class="literal"&gt;Linear_B</td><td><code class="literal">Lisu</code></td><td><code class="literal">Lycian</code></td></tr><tr><td><code class="literal">Lydian</code></td><td><code class="literal">Malayalam</code>&lt; /td&gt;</td><td><code class="literal">Mandaic</code></td><td><code class="literal">Meetei_Mayek</code></td><td><code class="literal">Meroitic_Cursive</code></td></tr><tr><td><code class="literal">Meroitic_Hieroglyphs</code></td><td><code class="literal">Miao</code></td><td><code class="literal">Mongolian</code></td><td><code class="literal">Myanmar</code></td><td><code class="literal">New_Tai_Lue</code></td></tr><tr><td><code class="literal">Nko</code></td><td><code class="literal">Ogham</code></td><td><code class="literal">Old_Italic</code></td><td><code class="literal">Old_Persian&lt; /code&gt;</code></td><td><code class="literal">Old_South_Arabian</code></td></tr><tr><td><code class="literal">Old_Turkic</code></td><td><code class="literal">Ol_Chiki</code></td><td><code class="literal">Oriya</code></td><td><code class="literal">Osmanya</code></td><td><code class="literal">Phags_Pa</code></td></tr><tr><td><code class="literal ">Phoenician</code></td><td><code class="literal">Rejang</code></td><td><code class="literal">Runic</code></td><td><code class="literal">Samaritan</code></td><td><code class="literal">Saurashtra</code></td></tr><tr><td><code class="literal">Sharada</code></td><td><code class="literal">Shavian</code></td><td><code class="literal">Sinhala</code></td><td><code class="literal">Sora_Sompeng</code></td><td><code class="literal">Sundanese</code></td></tr><tr><td><code class="literal">Syloti_Nagri</code></td><td><code class="literal">Syriac</code></td><td><code class="literal">Tagalog</code></td><td><code class="literal">Tagbanwa</code></td><td><code class="literal">Tai_Le</code></td></tr><tr><td><code class="literal">Tai_Tham</code></td><td><code class="literal">Tai_Viet</code></td><td><code class="literal">Takri</code></td><td><code class="literal">Tamil</code></td><td><code class=" literal">Telugu</code></td></tr><tr><td><code class="literal">Thaana</code></td><td><code class="literal">Thai</code></td><td><code class="literal">Tibetan</code></td><td><code class="literal">Tifinagh</code></td></tr><tr><td><code class="literal">Vai</code></td><td>&lt; code class="literal"&gt;Yi</td><td class="empty">&nbsp;</td><td class="empty">&nbsp;</td><td class="empty">&nbsp;</td><td class="empty">&nbsp;</td></tr></tbody></table>

`\X` знаходить розширений Unicode графемний кластер. Розширений графемний кластер — це один або кілька символів Unicode, які об'єднуються в один символьний знак (гліф). По суті, його можна розглядати як Unicode еквівалент для , оскільки він знаходить один незалежний комплексний символ, незалежно від того, скільки окремих символів використовується для його малювання.

Для версій PCRE до 8.32 (що відповідає версіям PHP до 5.4.14 під час використання вбудованої бібліотеки PCRE), `\X`равносилен`(?>\PM\pM*)`. Таким чином, він шукає символи без властивості "mark", і розглядає послідовність як атомарну групу (див. нижче). Символи з властивістю "mark" зазвичай є відмітними ознаками, які впливають на попередній символ.

Збіг символів за Unicode властивістю не є швидкою операцією, тому для цієї мети PCRE необхідно здійснити пошук у структурі даних з більш ніж 15 тисяч символів. Тому традиційні керуючі послідовності в PCRE, такі як `\d`и`\w`не використовують Unicode властивості.
