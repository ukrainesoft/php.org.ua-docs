---
navigation:
  - regexp.reference.back-references.md: « Зворотні посилання
  - regexp.reference.onlyonce.md: Одноразові підмаски »
  - index.md: PHP Manual
  - reference.pcre.pattern.syntax.md: Опис синтаксису Perl-сумісних регулярних виразів
title: Твердження
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Твердження

Твердження - це перевірки щодо символів, що йдуть до або після поточної позиції зіставлення, нічого при цьому не поглинаючи (ніякі символи вихідного тексту не ставляться у відповідність до тверджень). Найбільш прості варіанти тверджень, наприклад, \\b,\\B,\\A,\\Z,\\z, ^ і $ розглянуті в [escape-послідовності](regexp.reference.escape.md). Більш складні твердження записуються як підмаски. Твердження бувають двох видів: ті, що аналізують текст, наступний *після поточної позиції* (look ahead), та ідучий *перед нею*(look behind).

Зіставлення підмаски, що містить твердження, відбувається звичайним чином, крім того, що поточна позиція не змінюється. Твердження щодо *наступного тексту* починаються з (?= для позитивних тверджень і з (?! для заперечних тверджень. Наприклад, `\w+(?=;)` збігається зі словом, за яким слідує символ «;», але при цьому сама точка з комою до збігу не включається. А `foo(?!bar)` відповідає будь-якій появі "foo", після якої не йде "bar". Зауважимо, що схожий шаблон `(?!foo)bar` не шукатиме входження «bar», якому передує будь-який рядок за винятком «foo». Проте він відповідатиме будь-яким входженням підрядка «bar», оскільки умова (?!foo) завжди \*\*`true`\*\*якщо наступні три символи — «bar». Для отримання бажаного результату необхідно скористатися другою категорією тверджень.

Твердження щодо *попереднього тексту* починаються з (?<= для позитивних тверджень і (?(?<!foo)bar знайде входження "bar", яким не передує "foo". Самі твердження «назад» обмежені так, щоб усі підрядки, яким вони відповідають, мали фіксовану довжину. Але, якщо використовуються кілька альтернатив, вони повинні мати однакову довжину. Таким чином шаблон `(?<=bullock|donkey)`корректен, но`(?<!dogs?|cats?)` викликає помилку під час компіляції. Гілки, які відповідають рядкам різної довжини, дозволені лише на верхньому рівні тверджень щодо попереднього тексту. Це розширення щодо Perl 5.005, який вимагає, щоб усі гілки відповідали рядкам однакової довжини. Таке твердження як `(?<=ab(c|de))` не коректно, оскільки верхній рівень маски може відповідати рядкам різної довжини, але його можна перетворити на коректний шаблон, використовуючи альтернативи на верхньому рівні: `(?<=abc|abde)` Затвердження щодо попереднього тексту реалізовані так, що для кожної альтернативи поточна позиція тимчасово переноситься назад, на фіксовану ширину, після чого виконується пошук відповідності умові. Якщо перед поточною позицією недостатньо символів, пошук відповідності зазнає невдачі. Твердження назад у поєднанні з одноразовими підмасками можуть бути особливо зручними для пошуку в кінці рядка; відповідний приклад наведено в кінці розділу «Одноразові підмаски».

Декілька тверджень (різних типів) можуть бути присутніми у затвердженні, наприклад: `(?<=\d{3})(?<!999)foo` збігається з підрядком "foo", якому передують три цифри, відмінні від "999". Слід розуміти, що кожне із тверджень перевіряється щодо однієї і тієї ж позиції в тексті, що обробляється. Спочатку виконується перевірка того, що попередні три символи — це цифри, потім перевіряється, щоб ці цифри не були числом 999. Наведений вище шаблон не відповідає підстроці «foo», якій передують шість символів, перші три з яких — цифри, а останні три не утворюють "999". Наприклад, він не відповідає рядку «123abcfoo», тоді як шаблон `(?<=\d{3}...)(?<!999)foo` відповідає.

У цьому випадку аналізуються попередні шість символів щодо того, щоб перші три з них були цифрами, а останні три не утворили «999».

Твердження можуть бути вкладеними, причому у довільних поєднаннях: `(?<=(?<!foo)bar)baz` відповідає підрядку «baz», якому передує «bar», перед яким, у свою чергу, немає «foo», а `(?<=\d{3}...(?<!999))foo` — зовсім інший шаблон, що відповідає підрядку «foo», якому передують три цифри та три довільні символи, відмінні від «999».

Стверджуючі підмаски є незахоплюючими і неповторними, оскільки безглуздо повторювати те саме кілька разів. Якщо у твердженні довільного типу знаходиться захоплююча підмаска, вона нумерується в тій же послідовності, що й інші захоплюючі підмаски, але захоплення відповідних значень відбувається тільки для позитивних тверджень, оскільки для тих, хто заперечує це не має сенсу.

У твердженнях обробляється не більше 200 захоплюючих підмасок.
