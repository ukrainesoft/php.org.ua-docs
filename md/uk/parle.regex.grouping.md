---
navigation:
  - parle.regex.anchors.md: « Якоря
  - parle.examples.md: Приклади »
  - index.md: PHP Manual
  - parle.pattern.matching.md: Зіставлення з шаблоном
title: Угруповання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Угруповання

**Угруповання**

| Последовательность | Опис |
| --- | --- |
| (...) | Згрупувати регулярний вираз, щоб перевизначити пріоритет оператора за промовчанням. |
| (?r-s:pattern) | Застосувати опцію r та опустіть опцію s під час інтерпретації шаблону. Параметри можуть бути нулем або більше символів i, s або x. |
| **Опції** |  |
| Опція | Опис |
| \--- | \--- |
| i | Без урахування регістру. |
| \-i | З урахуванням регістру. |
| s | Змінює значення ".", щоб відповідати будь-якому символу. |
| \-s | змінює значення ".", щоб відповідати будь-якому символу крім "\\n". |
| x | Ігнорує коментарі та пробіли у шаблонах. Пробіли ігноруються, якщо вони не екрановані зворотною косою рисою, не містяться у "" або не з'являються всередині діапазону символів. |

Ці параметри можуть застосовуватися глобально лише на рівні правил шляхом передачі комбінації бітових прапорів в лексер. | | (? # comment) | Пропускає все, що знаходиться усередині (). Перший зустрінутий символ) завершує шаблон. Коментар не може містити символ а). Коментар може займати рядки. |
