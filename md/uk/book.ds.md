---
navigation:
  - function.untaint.md: « untaint
  - intro.ds.md: Вступ "
  - index.md: PHP Manual
  - refs.basic.other.md: Інші базові модулі
title: Структури даних
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Структури даних

-   [Вступ](intro.ds.md)
-   [Встановлення та налаштування](ds.setup.md)
    -   [Вимоги](ds.requirements.md)
    -   [Установка](ds.installation.md)
-   [Обумовлені константи](ds.constants.md)
-   [Приклади](ds.examples.md)
-   [Ds\\Collection](class.ds-collection.md) \- Інтерфейс Collection
    -   [Ds\\Collection::clear](ds-collection.clear.md) \- Видаляє всі значення
    -   [Ds\\Collection::copy](ds-collection.copy.md)— Повертає копію колекції
    -   [Ds\\Collection::isEmpty](ds-collection.isempty.md)— Перевіряє, чи колекція порожня.
    -   [Ds\\Collection::toArray](ds-collection.toarray.md)— Перетворює колекцію на масив (array)
-   [Ds\\Hashable](class.ds-hashable.md) \- Інтерфейс Hashable
    -   [Ds\\Hashable::equals](ds-hashable.equals.md)— Визначає, чи дорівнює поточний екземпляр переданому об'єкту
    -   [Ds\\Hashable::hash](ds-hashable.hash.md)— Повертає скалярне значення для використання як значення хешу
-   [Ds\\Sequence](class.ds-sequence.md) \- Інтерфейс Sequence
    -   [Ds\\Sequence::allocate](ds-sequence.allocate.md)— Виділення пам'яті під зазначену місткість
    -   [Ds\\Sequence::apply](ds-sequence.apply.md)— Оновлення всіх значень застосуванням переданої callback-функції до них
    -   [Ds\\Sequence::capacity](ds-sequence.capacity.md)— Повертає поточну місткість
    -   [Ds\\Sequence::contains](ds-sequence.contains.md)— Перевіряє, чи містяться в колекції задані значення
    -   [Ds\\Sequence::filter](ds-sequence.filter.md)— Створює нову послідовність елементів, вибраних за допомогою заданої callback-функції
    -   [Ds\\Sequence::find](ds-sequence.find.md) \- Пошук індексу за значенням
    -   [Ds\\Sequence::first](ds-sequence.first.md)— Повертає перший елемент колекції
    -   [Ds\\Sequence::get](ds-sequence.get.md)— Повертає значення за індексом
    -   [Ds\\Sequence::insert](ds-sequence.insert.md)— Вставляє значення за вказаним індексом
    -   [Ds\\Sequence::join](ds-sequence.join.md) \- Склеює всі значення в рядок
    -   [Ds\\Sequence::last](ds-sequence.last.md)— Повертає останнє значення колекції
    -   [Ds\\Sequence::map](ds-sequence.map.md)— Повертає результат застосування callback-функції до всіх значень колекції.
    -   [Ds\\Sequence::merge](ds-sequence.merge.md)— Повертає результат додавання всіх заданих значень до колекції
    -   [Ds\\Sequence::pop](ds-sequence.pop.md)— Видаляє та повертає останнє значення
    -   [Ds\\Sequence::push](ds-sequence.push.md)— Додає значення до кінця послідовності
    -   [Ds\\Sequence::reduce](ds-sequence.reduce.md) \- Сплескує колекцію до одного значення використовуючи callback-функцію
    -   [Ds\\Sequence::remove](ds-sequence.remove.md)— Видаляє та повертає значення за індексом
    -   [Ds\\Sequence::reverse](ds-sequence.reverse.md)— Перевертає поточну колекцію
    -   [Ds\\Sequence::reversed](ds-sequence.reversed.md)— Повертає перегорнуту копію колекції
    -   [Ds\\Sequence::rotate](ds-sequence.rotate.md)— Перемотує послідовність на задану кількість значень
    -   [Ds\\Sequence::set](ds-sequence.set.md)— Замінює значення за вказаним індексом
    -   [Ds\\Sequence::shift](ds-sequence.shift.md)— Видаляє та повертає перше значення
    -   [Ds\\Sequence::slice](ds-sequence.slice.md)— Повертає під-колекцію із заданого діапазону
    -   [Ds\\Sequence::sort](ds-sequence.sort.md)— Сортує колекцію
    -   [Ds\\Sequence::sorted](ds-sequence.sorted.md)— Повертає копію колекції, відсортовану за значенням.
    -   [Ds\\Sequence::sum](ds-sequence.sum.md)— Повертає суму всіх значень колекції
    -   [Ds\\Sequence::unshift](ds-sequence.unshift.md)— Додає значення на початок послідовності
-   [Ds\\Vector](class.ds-vector.md) \- Клас Vector
    -   [Ds\\Vector::allocate](ds-vector.allocate.md)— Виділяє пам'ять під зазначену місткість
    -   [Ds\\Vector::apply](ds-vector.apply.md) \- Оновлює всі значення, застосовуючи до них передану callback-функцію
    -   [Ds\\Vector::capacity](ds-vector.capacity.md)— Повертає поточну місткість
    -   [Ds\\Vector::clear](ds-vector.clear.md) \- Видаляє всі значення
    -   [Ds\\Vector::\_\_construct](ds-vector.construct.md) \- Створює новий екземпляр
    -   [Ds\\Vector::contains](ds-vector.contains.md)— Перевіряє, чи міститься у векторі задані значення
    -   [Ds\\Vector::copy](ds-vector.copy.md)— Повертає поверхневу копію вектора
    -   [Ds\\Vector::count](ds-vector.count.md)— Повертає кількість елементів вектора
    -   [Ds\\Vector::filter](ds-vector.filter.md)— Створює новий вектор із елементів, вибраних за допомогою заданої callback-функції
    -   [Ds\\Vector::find](ds-vector.find.md) \- Пошук індексу за значенням
    -   [Ds\\Vector::first](ds-vector.first.md)— Повертає перший елемент вектора
    -   [Ds\\Vector::get](ds-vector.get.md)— Повертає значення за індексом
    -   [Ds\\Vector::insert](ds-vector.insert.md)— Вставляє значення за вказаним індексом
    -   [Ds\\Vector::isEmpty](ds-vector.isempty.md)— Перевіряє, чи вектор порожній.
    -   [Ds\\Vector::join](ds-vector.join.md) \- Склеює всі значення в рядок
    -   [Ds\\Vector::jsonSerialize](ds-vector.jsonserialize.md)— Повертає вектор у JSON-представництві
    -   [Ds\\Vector::last](ds-vector.last.md)— Повертає останнє значення вектора
    -   [Ds\\Vector::map](ds-vector.map.md)— Повертає результат застосування callback-функції до всіх значень вектора
    -   [Ds\\Vector::merge](ds-vector.merge.md)— Повертає результат додавання всіх заданих значень у вектор.
    -   [Ds\\Vector::pop](ds-vector.pop.md)— Видаляє та повертає останнє значення
    -   [Ds\\Vector::push](ds-vector.push.md)— Додає значення до кінця вектора
    -   [Ds\\Vector::reduce](ds-vector.reduce.md) \- Зменшує вектор до одного значення, використовуючи callback-функцію
    -   [Ds\\Vector::remove](ds-vector.remove.md)— Видаляє та повертає значення за індексом
    -   [Ds\\Vector::reverse](ds-vector.reverse.md)— Перевертає поточний вектор
    -   [Ds\\Vector::reversed](ds-vector.reversed.md)— Повертає перегорнуту копію вектора
    -   [Ds\\Vector::rotate](ds-vector.rotate.md)— Перемотує вектор на задану кількість значень
    -   [Ds\\Vector::set](ds-vector.set.md)— Замінює значення за вказаним індексом
    -   [Ds\\Vector::shift](ds-vector.shift.md)— Видаляє та повертає перше значення
    -   [Ds\\Vector::slice](ds-vector.slice.md)— Повертає підвектор із заданого діапазону
    -   [Ds\\Vector::sort](ds-vector.sort.md)— Сортує вектор
    -   [Ds\\Vector::sorted](ds-vector.sorted.md)— Повертає копію колекції, відсортовану за значенням.
    -   [Ds\\Vector::sum](ds-vector.sum.md)— Повертає суму всіх значень колекції
    -   [Ds\\Vector::toArray](ds-vector.toarray.md)— Перетворює колекцію на масив (array)
    -   [Ds\\Vector::unshift](ds-vector.unshift.md)— Додає значення на початок вектора
-   [Ds\\Deque](class.ds-deque.md) \- Клас Deque
    -   [Ds\\Deque::allocate](ds-deque.allocate.md)— Виділяє пам'ять під зазначену місткість
    -   [Ds\\Deque::apply](ds-deque.apply.md) \- Оновлює всі значення, застосовуючи callback-функцію до кожного значення
    -   [Ds\\Deque::capacity](ds-deque.capacity.md)— Повертає поточну місткість
    -   [Ds\\Deque::clear](ds-deque.clear.md)— Видаляє всі значення із двосторонньої черги
    -   [Ds\\Deque::\_\_construct](ds-deque.construct.md) \- Створює новий екземпляр
    -   [Ds\\Deque::contains](ds-deque.contains.md)— Перевіряє, чи є у двосторонній черзі задані значення
    -   [Ds\\Deque::copy](ds-deque.copy.md)— Повертає поверхневу копію колекції
    -   [Ds\\Deque::count](ds-deque.count.md)— Повертає кількість елементів двосторонньої черги
    -   [Ds\\Deque::filter](ds-deque.filter.md)— Створює нову двосторонню чергу з елементів, вибраних за допомогою заданої callback-функції
    -   [Ds\\Deque::find](ds-deque.find.md) \- Пошук індексу за значенням
    -   [Ds\\Deque::first](ds-deque.first.md)— Повертає перший елемент двосторонньої черги
    -   [Ds\\Deque::get](ds-deque.get.md)— Повертає значення за індексом
    -   [Ds\\Deque::insert](ds-deque.insert.md)— Вставляє значення за вказаним індексом
    -   [Ds\\Deque::isEmpty](ds-deque.isempty.md)— Перевіряє, чи порожня двостороння черга
    -   [Ds\\Deque::join](ds-deque.join.md) \- Склеює всі значення в рядок
    -   [Ds\\Deque::jsonSerialize](ds-deque.jsonserialize.md)— Повертає колекцію в JSON-представництві
    -   [Ds\\Deque::last](ds-deque.last.md)— Повертає останнє значення двосторонньої черги
    -   [Ds\\Deque::map](ds-deque.map.md)— Повертає результат застосування callback-функції до всіх значень двосторонньої черги
    -   [Ds\\Deque::merge](ds-deque.merge.md)— Повертає результат додавання всіх заданих значень у двосторонню чергу
    -   [Ds\\Deque::pop](ds-deque.pop.md)— Видаляє та повертає останнє значення
    -   [Ds\\Deque::push](ds-deque.push.md)— Додає значення наприкінці двосторонньої черги
    -   [Ds\\Deque::reduce](ds-deque.reduce.md) \- Зменшує колекцію до одного значення, використовуючи callback-функцію
    -   [Ds\\Deque::remove](ds-deque.remove.md)— Видаляє та повертає значення за індексом
    -   [Ds\\Deque::reverse](ds-deque.reverse.md)— Перевертає поточну двосторонню чергу
    -   [Ds\\Deque::reversed](ds-deque.reversed.md)— Повертає перегорнуту копію двосторонньої черги
    -   [Ds\\Deque::rotate](ds-deque.rotate.md)— Перемотує двосторонню чергу на задану кількість значень
    -   [Ds\\Deque::set](ds-deque.set.md)— Замінює значення за вказаним індексом
    -   [Ds\\Deque::shift](ds-deque.shift.md)— Видаляє та повертає перше значення
    -   [Ds\\Deque::slice](ds-deque.slice.md)— Повертає почергово із заданого діапазону
    -   [Ds\\Deque::sort](ds-deque.sort.md)— Сортує двосторонню чергу
    -   [Ds\\Deque::sorted](ds-deque.sorted.md)— Повертає відсортовану за значенням копію двосторонньої черги
    -   [Ds\\Deque::sum](ds-deque.sum.md)— Повертає суму всіх значень двосторонньої черги
    -   [Ds\\Deque::toArray](ds-deque.toarray.md) \- Перетворює двосторонню чергу на масив (array)
    -   [Ds\\Deque::unshift](ds-deque.unshift.md)— Додає значення на початок двосторонньої черги
-   [Ds\\Map](class.ds-map.md) \- Клас Map
    -   [Ds\\Map::allocate](ds-map.allocate.md)— Виділяє необхідну кількість пам'яті під потрібну місткість
    -   [Ds\\Map::apply](ds-map.apply.md)— Оновлення всіх значень застосуванням переданої callback-функції до них
    -   [Ds\\Map::capacity](ds-map.capacity.md)— Повертає поточну місткість
    -   [Ds\\Map::clear](ds-map.clear.md)— Видаляє всі значення з колекції
    -   [Ds\\Map::\_\_construct](ds-map.construct.md) \- Створює новий екземпляр
    -   [Ds\\Map::copy](ds-map.copy.md)— Повертає поверхневу копію колекції
    -   [Ds\\Map::count](ds-map.count.md)— Повертає кількість елементів колекції
    -   [Ds\\Map::diff](ds-map.diff.md)— Створює нову колекцію пар із елементами, ключів яких немає в іншій колекції пар
    -   [Ds\\Map::filter](ds-map.filter.md)— Створює нову колекцію пар із елементів, вибраних за допомогою заданої callback-функції
    -   [Ds\\Map::first](ds-map.first.md)— Повертає перший елемент колекції
    -   [Ds\\Map::get](ds-map.get.md)— Повертає значення за ключом
    -   [Ds\\Map::hasKey](ds-map.haskey.md)— Перевіряє, чи колекція містить заданий ключ
    -   [Ds\\Map::hasValue](ds-map.hasvalue.md)— Перевіряє, чи колекція містить задане значення
    -   [Ds\\Map::intersect](ds-map.intersect.md)— Створює нову колекцію пар, створену перетином з іншою колекцією пар
    -   [Ds\\Map::isEmpty](ds-map.isempty.md)— Перевіряє, чи колекція порожня.
    -   [Ds\\Map::jsonSerialize](ds-map.jsonserialize.md)— Повертає колекцію в JSON-представництві
    -   [Ds\\Map::keys](ds-map.keys.md)— Повертає набір ключів колекції
    -   [Ds\\Map::ksort](ds-map.ksort.md)— Сортує поточну колекцію за ключами
    -   [Ds\\Map::ksorted](ds-map.ksorted.md)— Повертає копію колекції, відсортованої за ключами
    -   [Ds\\Map::last](ds-map.last.md)— Повертає останню пару колекції
    -   [Ds\\Map::map](ds-map.map.md)— Повертає результат застосування callback-функції до всіх значень колекції.
    -   [Ds\\Map::merge](ds-map.merge.md)— Повертає результат додавання всіх заданих елементів до колекції
    -   [Ds\\Map::pairs](ds-map.pairs.md)— Повертає послідовність, яка містить усі пари колекції.
    -   [Ds\\Map::put](ds-map.put.md)— Встановлення значення за заданим ключем
    -   [Ds\\Map::putAll](ds-map.putall.md)— Зв'язує з колекцією всі пари ключ-значення з об'єкту класу traversable чи масиву
    -   [Ds\\Map::reduce](ds-map.reduce.md) \- Зменшує колекцію до одного значення, використовуючи callback-функцію
    -   [Ds\\Map::remove](ds-map.remove.md)— Видаляє та повертає значення за ключом
    -   [Ds\\Map::reverse](ds-map.reverse.md)— Перевертає поточну колекцію
    -   [Ds\\Map::reversed](ds-map.reversed.md)— Повертає перегорнуту копію колекції
    -   [Ds\\Map::skip](ds-map.skip.md)— Повертає пару за індексом позиції
    -   [Ds\\Map::slice](ds-map.slice.md)— Повертає підмножину колекції із заданого діапазону
    -   [Ds\\Map::sort](ds-map.sort.md)— Сортує колекцію за значеннями
    -   [Ds\\Map::sorted](ds-map.sorted.md)— Повертає копію колекції, відсортовану за значенням.
    -   [Ds\\Map::sum](ds-map.sum.md)— Повертає суму всіх значень колекції
    -   [Ds\\Map::toArray](ds-map.toarray.md)— Перетворює колекцію на масив (array)
    -   [Ds\\Map::union](ds-map.union.md)— Створює нову колекцію пар із елементів двох колекцій
    -   [Ds\\Map::values](ds-map.values.md)— Повертає послідовність значень колекції
    -   [Ds\\Map::xor](ds-map.xor.md)— Створює нову колекцію пар із елементів, які є в одній із колекцій, але не в обох одночасно
-   [Ds\\Pair](class.ds-pair.md) \- Клас Pair
    -   [Ds\\Pair::clear](ds-pair.clear.md) \- Видаляє всі значення
    -   [Ds\\Pair::\_\_construct](ds-pair.construct.md) \- Створює екземпляр класу
    -   [Ds\\Pair::copy](ds-pair.copy.md)— Повертає поверхневу копію пари
    -   [Ds\\Pair::isEmpty](ds-pair.isempty.md)— Перевіряє, чи пара порожня.
    -   [Ds\\Pair::jsonSerialize](ds-pair.jsonserialize.md)— Повертає пару у виставі JSON
    -   [Ds\\Pair::toArray](ds-pair.toarray.md) \- Перетворює пару в масив (array)
-   [Ds\\Set](class.ds-set.md) \- Клас Set
    -   [Ds\\Set::add](ds-set.add.md)— Додає значення до набору
    -   [Ds\\Set::allocate](ds-set.allocate.md)— Виділяє пам'ять під зазначену місткість
    -   [Ds\\Set::capacity](ds-set.capacity.md)— Повертає поточну місткість
    -   [Ds\\Set::clear](ds-set.clear.md)— Видаляє всі значення з колекції
    -   [Ds\\Set::\_\_construct](ds-set.construct.md) \- Створює новий екземпляр класу
    -   [Ds\\Set::contains](ds-set.contains.md)— Перевіряє, чи міститься в колекції задані значення
    -   [Ds\\Set::copy](ds-set.copy.md)— Повертає поверхневу копію колекції
    -   [Ds\\Set::count](ds-set.count.md)— Повертає кількість елементів колекції
    -   [Ds\\Set::diff](ds-set.diff.md)— Створює новий набір із елементами, яких немає в іншому наборі
    -   [Ds\\Set::filter](ds-set.filter.md)— Створює новий список із елементів, вибраних за допомогою заданої callback-функції
    -   [Ds\\Set::first](ds-set.first.md)— Повертає перший елемент колекції
    -   [Ds\\Set::get](ds-set.get.md)— Повертає значення за індексом
    -   [Ds\\Set::intersect](ds-set.intersect.md)— Створює новий набір, створений перетином з іншим набором
    -   [Ds\\Set::isEmpty](ds-set.isempty.md)— Перевіряє, чи колекція порожня.
    -   [Ds\\Set::join](ds-set.join.md) \- Склеює всі значення в рядок
    -   [Ds\\Set::jsonSerialize](ds-set.jsonserialize.md)— Повертає колекцію в JSON-представництві
    -   [Ds\\Set::last](ds-set.last.md)— Повертає останнє значення колекції
    -   [Ds\\Set::merge](ds-set.merge.md)— Повертає результат додавання всіх заданих значень до набору
    -   [Ds\\Set::reduce](ds-set.reduce.md) \- Зменшує колекцію до одного значення, використовуючи callback-функцію
    -   [Ds\\Set::remove](ds-set.remove.md)— Видаляє всі задані значення набору
    -   [Ds\\Set::reverse](ds-set.reverse.md)— Перевертає поточну колекцію
    -   [Ds\\Set::reversed](ds-set.reversed.md)— Повертає перегорнуту копію колекції
    -   [Ds\\Set::slice](ds-set.slice.md)— Повертає піднабір із заданого діапазону
    -   [Ds\\Set::sort](ds-set.sort.md)— Сортує колекцію
    -   [Ds\\Set::sorted](ds-set.sorted.md)— Повертає копію колекції, відсортовану за значенням.
    -   [Ds\\Set::sum](ds-set.sum.md)— Повертає суму всіх значень колекції
    -   [Ds\\Set::toArray](ds-set.toarray.md)— Перетворює колекцію на масив (array)
    -   [Ds\\Set::union](ds-set.union.md)— Створює новий набір з елементів поточного та переданого наборів
    -   [Ds\\Set::xor](ds-set.xor.md)— Створює новий набір із значень, які є в одному з наборів, але не в обох одночасно
-   [Ds\\Stack](class.ds-stack.md) \- Клас Stack
    -   [Ds\\Stack::allocate](ds-stack.allocate.md)— Виділяє пам'ять під зазначену місткість
    -   [Ds\\Stack::capacity](ds-stack.capacity.md)— Повертає поточну місткість
    -   [Ds\\Stack::clear](ds-stack.clear.md)— Видаляє всі значення з колекції
    -   [Ds\\Stack::\_\_construct](ds-stack.construct.md) \- Створює новий екземпляр класу
    -   [Ds\\Stack::copy](ds-stack.copy.md)— Повертає поверхневу копію колекції
    -   [Ds\\Stack::count](ds-stack.count.md)— Повертає кількість елементів колекції
    -   [Ds\\Stack::isEmpty](ds-stack.isempty.md)— Перевіряє, чи колекція порожня.
    -   [Ds\\Stack::jsonSerialize](ds-stack.jsonserialize.md)— Повертає колекцію в JSON-представництві
    -   [Ds\\Stack::peek](ds-stack.peek.md)— Повертає значення з вершини стека
    -   [Ds\\Stack::pop](ds-stack.pop.md)— Видаляє та повертає значення з вершини стека
    -   [Ds\\Stack::push](ds-stack.push.md)— Додає значення у стек
    -   [Ds\\Stack::toArray](ds-stack.toarray.md)— Перетворює колекцію на масив (array)
-   [Ds\\Queue](class.ds-queue.md) \- Клас Queue
    -   [Ds\\Queue::allocate](ds-queue.allocate.md)— Виділяє пам'ять під зазначену місткість
    -   [Ds\\Queue::capacity](ds-queue.capacity.md)— Повертає поточну місткість
    -   [Ds\\Queue::clear](ds-queue.clear.md) \- Видаляє всі значення
    -   [Ds\\Queue::\_\_construct](ds-queue.construct.md) \- Створює новий екземпляр
    -   [Ds\\Queue::copy](ds-queue.copy.md)— Повертає поверхневу копію черги
    -   [Ds\\Queue::count](ds-queue.count.md)— Повертає кількість елементів черги
    -   [Ds\\Queue::isEmpty](ds-queue.isempty.md)— Перевіряє, чи колекція порожня.
    -   [Ds\\Queue::jsonSerialize](ds-queue.jsonserialize.md)— Повертає колекцію в JSON-представництві
    -   [Ds\\Queue::peek](ds-queue.peek.md)— Повертає значення з початку черги
    -   [Ds\\Queue::pop](ds-queue.pop.md)— Видаляє та повертає значення з початку черги
    -   [Ds\\Queue::push](ds-queue.push.md)— Додає значення у чергу
    -   [Ds\\Queue::toArray](ds-queue.toarray.md)— Перетворює колекцію на масив (array)
-   [Ds\\PriorityQueue](class.ds-priorityqueue.md) \- Клас PriorityQueue
    -   [Ds\\PriorityQueue::allocate](ds-priorityqueue.allocate.md)— Виділяє пам'ять під зазначену місткість
    -   [Ds\\PriorityQueue::capacity](ds-priorityqueue.capacity.md)— Повертає поточну місткість
    -   [Ds\\PriorityQueue::clear](ds-priorityqueue.clear.md) \- Видаляє всі значення
    -   [Ds\\PriorityQueue::\_\_construct](ds-priorityqueue.construct.md) \- Створює новий екземпляр
    -   [Ds\\PriorityQueue::copy](ds-priorityqueue.copy.md)— Повертає поверхневу копію черги
    -   [Ds\\PriorityQueue::count](ds-priorityqueue.count.md)— Повертає кількість елементів у черзі
    -   [Ds\\PriorityQueue::isEmpty](ds-priorityqueue.isempty.md)— Перевіряє, чи колекція порожня.
    -   [Ds\\PriorityQueue::jsonSerialize](ds-priorityqueue.jsonserialize.md)— Повертає колекцію в JSON-виставу
    -   [Ds\\PriorityQueue::peek](ds-priorityqueue.peek.md)— Повертає значення з початку черги
    -   [Ds\\PriorityQueue::pop](ds-priorityqueue.pop.md)— Видаляє та повертає значення з найвищим пріоритетом
    -   [Ds\\PriorityQueue::push](ds-priorityqueue.push.md)— Додає значення у чергу
    -   [Ds\\PriorityQueue::toArray](ds-priorityqueue.toarray.md) \- Перетворює чергу на масив (array)
