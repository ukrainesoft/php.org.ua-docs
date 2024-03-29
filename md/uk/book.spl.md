---
navigation:
  - seaslog.warning.md: '« SeasLog::warning'
  - intro.spl.md: Вступ "
  - index.md: PHP Manual
  - refs.basic.other.md: Інші базові модулі
title: Стандартна бібліотека PHP (SPL)
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Стандартна бібліотека PHP (SPL)

-   [Вступ](intro.spl.md)
-   [Встановлення та налаштування](spl.setup.md)
    -   [Вимоги](spl.requirements.md)
    -   [Установка](spl.installation.md)
    -   [Налаштування під час виконання](spl.configuration.md)
    -   [Типи ресурсів](spl.resources.md)
-   [Обумовлені константи](spl.constants.md)
-   [Структури даних](spl.datastructures.md)
    -   [SplDoublyLinkedList](class.spldoublylinkedlist.md) \- Клас SplDoublyLinkedList
    -   [SplStack](class.splstack.md) \- Клас SplStack
    -   [SplQueue](class.splqueue.md) \- Клас SplQueue
    -   [SplHeap](class.splheap.md) \- Клас SplHeap
    -   [SplMaxHeap](class.splmaxheap.md) \- Клас SplMaxHeap
    -   [SplMinHeap](class.splminheap.md) \- Клас SplMinHeap
    -   [SplPriorityQueue](class.splpriorityqueue.md) \- Клас SplPriorityQueue
    -   [SplFixedArray](class.splfixedarray.md) \- Клас SplFixedArray
    -   [SplObjectStorage](class.splobjectstorage.md) \- Клас SplObjectStorage
-   [Ітератори](spl.iterators.md)
    -   [AppendIterator](class.appenditerator.md) \- Клас AppendIterator
    -   [ArrayIterator](class.arrayiterator.md) \- Клас ArrayIterator
    -   [CachingIterator](class.cachingiterator.md) \- Клас CachingIterator
    -   [CallbackFilterIterator](class.callbackfilteriterator.md) \- Клас CallbackFilterIterator
    -   [DirectoryIterator](class.directoryiterator.md) \- Клас DirectoryIterator
    -   [EmptyIterator](class.emptyiterator.md) \- Клас EmptyIterator
    -   [FilesystemIterator](class.filesystemiterator.md) \- Клас FilesystemIterator
    -   [FilterIterator](class.filteriterator.md) \- Клас FilterIterator
    -   [GlobIterator](class.globiterator.md) \- Клас GlobIterator
    -   [InfiniteIterator](class.infiniteiterator.md) \- Клас InfiniteIterator
    -   [IteratorIterator](class.iteratoriterator.md) \- Клас IteratorIterator
    -   [LimitIterator](class.limititerator.md) \- Клас LimitIterator
    -   [MultipleIterator](class.multipleiterator.md) \- Клас MultipleIterator
    -   [NoRewindIterator](class.norewinditerator.md) \- Клас NoRewindIterator
    -   [ParentIterator](class.parentiterator.md) \- Клас ParentIterator
    -   [RecursiveArrayIterator](class.recursivearrayiterator.md) \- Клас RecursiveArrayIterator
    -   [RecursiveCachingIterator](class.recursivecachingiterator.md) \- Клас RecursiveCachingIterator
    -   [RecursiveCallbackFilterIterator](class.recursivecallbackfilteriterator.md) \- Клас RecursiveCallbackFilterIterator
    -   [RecursiveDirectoryIterator](class.recursivedirectoryiterator.md)— Клас RecursiveDirectoryIterator
    -   [RecursiveFilterIterator](class.recursivefilteriterator.md) \- Клас RecursiveFilterIterator
    -   [RecursiveIteratorIterator](class.recursiveiteratoriterator.md) \- Клас RecursiveIteratorIterator
    -   [RecursiveRegexIterator](class.recursiveregexiterator.md) \- Клас RecursiveRegexIterator
    -   [RecursiveTreeIterator](class.recursivetreeiterator.md) \- Клас RecursiveTreeIterator
    -   [RegexIterator](class.regexiterator.md) \- Клас RegexIterator
-   [Інтерфейси](spl.interfaces.md)
    -   [Countable](class.countable.md) \- Інтерфейс Countable
    -   [OuterIterator](class.outeriterator.md) \- Інтерфейс OuterIterator
    -   [RecursiveIterator](class.recursiveiterator.md) \- Інтерфейс RecursiveIterator
    -   [SeekableIterator](class.seekableiterator.md) \- Інтерфейс SeekableIterator
-   [Винятки](spl.exceptions.md)
    -   [BadFunctionCallException](class.badfunctioncallexception.md) \- Клас BadFunctionCallException
    -   [BadMethodCallException](class.badmethodcallexception.md) \- Клас BadMethodCallException
    -   [DomainException](class.domainexception.md) \- Клас DomainException
    -   [InvalidArgumentException](class.invalidargumentexception.md) \- Клас InvalidArgumentException
    -   [LengthException](class.lengthexception.md) \- Клас LengthException
    -   [LogicException](class.logicexception.md) \- Клас LogicException
    -   [OutOfBoundsException](class.outofboundsexception.md) \- Клас OutOfBoundsException
    -   [OutOfRangeException](class.outofrangeexception.md) \- Клас OutOfRangeException
    -   [OverflowException](class.overflowexception.md) \- Клас OverflowException
    -   [RangeException](class.rangeexception.md) \- Клас RangeException
    -   [RuntimeException](class.runtimeexception.md) \- Клас RuntimeException
    -   [UnderflowException](class.underflowexception.md) \- Клас UnderflowException
    -   [UnexpectedValueException](class.unexpectedvalueexception.md) \- Клас UnexpectedValueException
-   [Функції SPL](ref.spl.md)
    -   [class\_implements](function.class-implements.md)— Повертає список інтерфейсів, реалізованих у заданому класі чи інтерфейсі
    -   [class\_parents](function.class-parents.md) \- Повертає список батьківських класів заданого класу
    -   [class\_uses](function.class-uses.md)— Повертає список трейтів, які використовуються заданим класом
    -   [iterator\_apply](function.iterator-apply.md)— Викликає функцію кожного елемента в ітераторі
    -   [iterator\_count](function.iterator-count.md)— Підраховує кількість елементів в ітераторі
    -   [iterator\_to\_array](function.iterator-to-array.md)— Копіює ітератор у масив
    -   [spl\_autoload\_call](function.spl-autoload-call.md)— Спроба завантажити клас усіма зареєстрованими функціями\_\_autoload()
    -   [spl\_autoload\_extensions](function.spl-autoload-extensions.md)— Реєстрація та виведення розширень файлів для spl\_autoload
    -   [spl\_autoload\_functions](function.spl-autoload-functions.md)— Отримання списку всіх зареєстрованих функцій\_\_autoload()
    -   [spl\_autoload\_register](function.spl-autoload-register.md)— Реєструє задану функцію як реалізацію методу\_\_autoload()
    -   [spl\_autoload\_unregister](function.spl-autoload-unregister.md)— Скасування реєстрації функції як реалізацію методу\_\_autoload()
    -   [spl\_autoload](function.spl-autoload.md) \- Реалізація за умовчанням методу\_\_autoload()
    -   [spl\_classes](function.spl-classes.md)— Повертає доступні класи SPL
    -   [spl\_object\_hash](function.spl-object-hash.md)— Повертає хеш-ідентифікатор об'єкту
    -   [spl\_object\_id](function.spl-object-id.md)— Отримати цілий ідентифікатор об'єкта
-   [Обробка файлів](spl.files.md)
    -   [SplFileInfo](class.splfileinfo.md) \- Клас SplFileInfo
    -   [SplFileObject](class.splfileobject.md) \- Клас SplFileObject
    -   [SplTempFileObject](class.spltempfileobject.md) \- Клас SplTempFileObject
-   [Різні класи та інтерфейси](spl.misc.md)
    -   [ArrayObject](class.arrayobject.md) \- Клас ArrayObject
    -   [SplObserver](class.splobserver.md) \- Інтерфейс SplObserver
    -   [SplSubject](class.splsubject.md) \- Інтерфейс SplSubject
