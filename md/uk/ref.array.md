---
navigation:
  - array.sorting.md: « Сортування масивів
  - function.array-change-key-case.md: array\_change\_key\_case »
  - index.md: PHP Manual
  - book.array.md: Масиви
title: Функції для роботи з масивами
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Функції для роботи з масивами

# Дивіться також

Смотрите также[is\_array()](function.is-array.md) [explode()](function.explode.md) [implode()](function.implode.md) [preg\_split()](function.preg-split.md) і [unset()](function.unset.md)

## Зміст

-   [array\_change\_key\_case](function.array-change-key-case.md)— Змінює регістр усіх ключів у масиві
-   [array\_chunk](function.array-chunk.md) \- Розбиває масив на частини
-   [array\_column](function.array-column.md)— Повертає масив із значень одного стовпця вхідного масиву
-   [array\_combine](function.array-combine.md)— Створює новий масив, використовуючи один масив як ключі, а інший для його значень
-   [array\_count\_values](function.array-count-values.md)— Підраховує кількість входжень кожного окремого значення у масиві
-   [array\_diff\_assoc](function.array-diff-assoc.md)— Обчислює розбіжність масивів із додатковою перевіркою індексу
-   [array\_diff\_key](function.array-diff-key.md)— Обчислює розбіжність масивів, порівнюючи ключі
-   [array\_diff\_uassoc](function.array-diff-uassoc.md)— Обчислює розбіжність масивів з додатковою перевіркою індексу через пользовательскую callback-функцію
-   [array\_diff\_ukey](function.array-diff-ukey.md) \- Обчислює розбіжність масивів, використовуючи callback-функцію для порівняння ключів
-   [array\_diff](function.array-diff.md) \- Обчислює розбіжність масивів
-   [array\_fill\_keys](function.array-fill-keys.md)— створює масив і заповнює його значеннями з певними ключами.
-   [array\_fill](function.array-fill.md) \- Заповнює масив значеннями
-   [array\_filter](function.array-filter.md) \- Фільтрує елементи масиву за допомогою callback-функції
-   [array\_flip](function.array-flip.md)— Змінює місцями ключі з їхніми значеннями у масиві
-   [array\_intersect\_assoc](function.array-intersect-assoc.md)— Обчислює перетин масивів із додатковою перевіркою індексу
-   [array\_intersect\_key](function.array-intersect-key.md)— Обчислює перетин масивів, порівнюючи ключі
-   [array\_intersect\_uassoc](function.array-intersect-uassoc.md) \- Обчислює перетин масивів з додатковою перевіркою індексу, порівнюючи індекси через callback-функцію
-   [array\_intersect\_ukey](function.array-intersect-ukey.md) \- Обчислює перетин масивів, використовуючи callback-функцію для порівняння ключів
-   [array\_intersect](function.array-intersect.md) \- Обчислює перетин масивів
-   [array\_is\_list](function.array-is-list.md)— Перевіряє, чи цей array є списком
-   [array\_key\_exists](function.array-key-exists.md)— Перевіряє, чи існує у масиві заданий ключ чи індекс
-   [array\_key\_first](function.array-key-first.md)— Отримує перший ключ масиву
-   [array\_key\_last](function.array-key-last.md)— Отримує останній ключ масиву
-   [array\_keys](function.array-keys.md)— Повертає всі або деякі підмножини ключів масиву
-   [array\_map](function.array-map.md) \- Застосовує callback-функцію до всіх елементів зазначених масивів
-   [array\_merge\_recursive](function.array-merge-recursive.md)— Рекурсивне злиття одного чи більше масивів
-   [array\_merge](function.array-merge.md)— Зливає один або більше масивів
-   [array\_multisort](function.array-multisort.md)— Сортує кілька масивів чи багатовимірні масиви
-   [array\_pad](function.array-pad.md)— Доповнити масив певним значенням до вказаної довжини
-   [array\_pop](function.array-pop.md)— Витягує останній елемент масиву
-   [array\_product](function.array-product.md)— Обчислює добуток значень масиву
-   [array\_push](function.array-push.md)— Додає один або кілька елементів до кінця масиву
-   [array\_rand](function.array-rand.md)— Вибирає один чи кілька випадкових ключів із масиву
-   [array\_reduce](function.array-reduce.md) \- Ітеративно зменшує масив до єдиного значення, використовуючи callback-функцію
-   [array\_replace\_recursive](function.array-replace-recursive.md)— Рекурсивно замінює елементи першого масиву на елементи переданих масивів.
-   [array\_replace](function.array-replace.md)— Замінює елементи масиву елементами інших переданих масивів
-   [array\_reverse](function.array-reverse.md)— Повертає масив із елементами у зворотному порядку
-   [array\_search](function.array-search.md)— Здійснює пошук даного значення в масиві та повертає ключ першого знайденого елемента у разі успішного виконання
-   [array\_shift](function.array-shift.md)— Витягує перший елемент масиву
-   [array\_slice](function.array-slice.md) \- Вибирає зріз масиву
-   [array\_splice](function.array-splice.md)— Видаляє частину масиву і замінює її чимось ще
-   [array\_sum](function.array-sum.md)— Обчислює суму значень масиву
-   [array\_udiff\_assoc](function.array-udiff-assoc.md) \- Обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи для порівняння значень callback-функцію
-   [array\_udiff\_uassoc](function.array-udiff-uassoc.md) \- Обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи для порівняння значень та індексів callback-функцію
-   [array\_udiff](function.array-udiff.md) \- Обчислює розбіжність масивів, використовуючи для порівняння callback-функцію
-   [array\_uintersect\_assoc](function.array-uintersect-assoc.md) \- Обчислює перетин масивів з додатковою перевіркою індексів, використовуючи для порівняння значень callback-функцію
-   [array\_uintersect\_uassoc](function.array-uintersect-uassoc.md)— Обчислює перетин масивів з додатковою перевіркою індексу, використовуючи для порівняння індексів та значень окремі callback-функції
-   [array\_uintersect](function.array-uintersect.md) \- Обчислює перетин масивів, використовуючи для порівняння значень callback-функцію
-   [array\_unique](function.array-unique.md)— Прибирає значення, що повторюються, з масиву
-   [array\_unshift](function.array-unshift.md)— Додає один або кілька елементів на початок масиву
-   [array\_values](function.array-values.md)— Повертає всі значення масиву
-   [array\_walk\_recursive](function.array-walk-recursive.md)— Рекурсивно застосовує функцію користувача до кожного елементу масиву
-   [array\_walk](function.array-walk.md)— Застосовує задану користувачем функцію кожного елемента масиву
-   [array](function.array.md) \- Створює масив
-   [arsort](function.arsort.md)— Сортує масив у порядку зменшення, зберігаючи асоціацію індексів
-   [asort](function.asort.md)— Сортує масив у порядку зростання, зберігаючи асоціацію індексів
-   [compact](function.compact.md)— Створює масив, що містить назви змінних та їх значення
-   [count](function.count.md)— Підраховує кількість елементів масиву чи Countable об'єкті
-   [current](function.current.md)— Повертає поточний елемент масиву
-   [each](function.each.md)— Повертає поточну пару ключ/значення з масиву та зміщує його покажчик
-   [end](function.end.md) — Встановлює внутрішній покажчик масиву на останній елемент
-   [extract](function.extract.md)— Імпортує змінні масиву до поточної таблиці символів
-   [in\_array](function.in-array.md)— Перевіряє, чи є у масиві значення
-   [key\_exists](function.key-exists.md) \- Псевдонім array\_key\_exists
-   [key](function.key.md)— Вибирає ключ із масиву
-   [krsort](function.krsort.md)— Сортує масив за ключом у порядку зменшення
-   [ksort](function.ksort.md)— Сортує масив за ключом у порядку зростання
-   [list](function.list.md) \- Надає змінним значення схожим на масиви синтаксисом.
-   [natcasesort](function.natcasesort.md)— Сортує масив алгоритмом природного сортування (natural order) без урахування регістру символів
-   [natsort](function.natsort.md) - Сортує масив, використовуючи алгоритм "natural order"
-   [next](function.next.md)— Переміщує покажчик масиву вперед на один елемент
-   [pos](function.pos.md) \- Псевдонім current
-   [prev](function.prev.md)— Пересуває внутрішній покажчик масиву на одну позицію.
-   [range](function.range.md)— Створює масив, що містить діапазон елементів
-   [reset](function.reset.md) - Встановлює внутрішній покажчик масиву на перший елемент
-   [rsort](function.rsort.md)— Сортує масив у порядку зменшення
-   [shuffle](function.shuffle.md) \- Перемішує масив
-   [sizeof](function.sizeof.md) \- Псевдонім count
-   [sort](function.sort.md) \- Сортує масив за зростанням
-   [uasort](function.uasort.md)— Сортує масив користувальницькою функцією порівняння, зберігаючи асоціацію індексів
-   [uksort](function.uksort.md)— Сортує масив за ключами користувальницькою функцією порівняння
-   [usort](function.usort.md)— Сортує масив за значеннями використовуючи функцію користувача для порівняння елементів
