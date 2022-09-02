---
navigation:
  - function.usleep.md: « usleep
  - book.seaslog.md: Seaslog »
  - index.md: PHP Manual
  - book.misc.md: Misc.
title: список змін
---
# список змін

Наступні зміни були здійснені з класами/функціями/методами даного модуля.

| Version | Function | Description |
| --- | --- | --- |
|  | [constant](function.constant.md) | Якщо константа не визначена, функція constant тепер викидає виняток Error; раніше видавалась помилка рівня EWARNING та поверталося значення null. |
|  | [define](function.define.md) | Передача true у випадкуinsensitive тепер видає помилку рівня EWARNING. Передача false все ще дозволена. |
|  | [ignoreuserabort](function.ignore-user-abort.md) | enable тепер допускає значення null. |
|  | [pack](function.pack.md) | Функція більше не повертає false у разі виникнення помилки. |
|  | [sapiwindowsvt100support](function.sapi-windows-vt100-support.md) | enable тепер допускає значення null. |
|  | [define](function.define.md) | Параметр caseinsensitive оголошено застарілим і буде видалено у версії 8.0.0. |
|  | [pack](function.pack.md) | Типи float і double підтримують як зворотний, і прямий порядок передачі байтів. |
|  | [unpack](function.unpack.md) | Типи float і double підтримують як зворотний, і прямий порядок передачі байтів. |
|  | [unpack](function.unpack.md) | Додано необов'язковий параметр offset. |
|  | [pack](function.pack.md) | Додані коди "e", "E", "g" та "G" для підтримки примусової вказівки порядку байт для float та double. |
|  | [define](function.define.md) | Допустимі значення типу array. |
