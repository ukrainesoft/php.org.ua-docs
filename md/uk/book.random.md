---
navigation:
  - changelog.misc.md: '" Список змін'
  - intro.random.md: Вступ "
  - index.md: PHP Manual
  - refs.basic.other.md: Інші базові модулі
title: 'Генератори випадкових чисел та функції, пов''язані з випадковістю'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Генератори випадкових чисел та функції, пов'язані з випадковістю

-   [Вступ](intro.random.md)
-   [Встановлення та налаштування](random.setup.md)
    -   [Вимоги](random.requirements.md)
    -   [Установка](random.installation.md)
    -   [Налаштування під час виконання](random.configuration.md)
    -   [Типи ресурсів](random.resources.md)
-   [Обумовлені константи](random.constants.md)
-   [Приклади](random.examples.md)
-   [Функції Random](ref.random.md)
    -   [getrandmax](function.getrandmax.md)— Повертає максимально можливе випадкове число
    -   [lcg\_value](function.lcg-value.md) \- Генерує псевдовипадкове число, застосовуючи комбінований лінійний конгруентний метод
    -   [mt\_getrandmax](function.mt-getrandmax.md)— Показує максимально можливе значення випадкового числа
    -   [mt\_rand](function.mt-rand.md)— Генерує випадкове значення методом за допомогою генератора простих чисел на базі Вихря Мерсенна
    -   [mt\_srand](function.mt-srand.md)— Ініціалізує генератор випадкових чисел на базі Вихря Мерсенна
    -   [rand](function.rand.md) \- Генерує випадкове число
    -   [random\_bytes](function.random-bytes.md)— Отримує криптографічно безпечні випадкові байти
    -   [random\_int](function.random-int.md)— Отримує криптографічно безпечне, рівномірно вибране ціле число
    -   [srand](function.srand.md) \- Задає початкову кількість генератора псевдовипадкових чисел
-   [Random\\Randomizer](class.random-randomizer.md) \- Клас Random\\Randomizer
    -   [Random\\Randomizer::\_\_construct](random-randomizer.construct.md)— Створює новий об'єкт Randomizer
    -   [Random\\Randomizer::getBytes](random-randomizer.getbytes.md)— Отримує випадкові байти
    -   [Random\\Randomizer::getBytesFromString](random-randomizer.getbytesfromstring.md)— Отримує випадкові байти з вихідного рядка
    -   [Random\\Randomizer::getFloat](random-randomizer.getfloat.md)— Отримує рівномірно обране число з плаваючою точкою
    -   [Random\\Randomizer::getInt](random-randomizer.getint.md)— Отримує рівномірно вибране ціле число
    -   [Random\\Randomizer::nextFloat](random-randomizer.nextfloat.md)— Отримує число з точкою, що плаває, з відкритого праворуч інтервалу\[
    -   [Random\\Randomizer::nextInt](random-randomizer.nextint.md)— Отримує ціле позитивне число
    -   [Random\\Randomizer::pickArrayKeys](random-randomizer.pickarraykeys.md) \- Вибирає випадкові ключі масиву
    -   [Random\\Randomizer::\_\_serialize](random-randomizer.serialize.md) \- Серіалізує об'єкт Randomizer
    -   [Random\\Randomizer::shuffleArray](random-randomizer.shufflearray.md)— Отримує перестановку масиву
    -   [Random\\Randomizer::shuffleBytes](random-randomizer.shufflebytes.md)— Отримує байтову перестановку рядка
    -   [Random\\Randomizer::\_\_unserialize](random-randomizer.unserialize.md)— Десеріалізує параметр data в об'єкті Randomizer
-   [Random\\Engine](class.random-engine.md) \- Інтерфейс Random\\Engine
    -   [Random\\Engine::generate](random-engine.generate.md) \- Створює випадкову послідовність
-   [Random\\CryptoSafeEngine](class.random-cryptosafeengine.md) \- Інтерфейс Random\\CryptoSafeEngine
-   [Random\\Engine\\Secure](class.random-engine-secure.md) \- Клас Random\\Engine\\Secure
    -   [Random\\Engine\\Secure::generate](random-engine-secure.generate.md)— Створює криптографічно безпечну випадкову послідовність
-   [Random\\Engine\\Mt19937](class.random-engine-mt19937.md) \- Клас Random\\Engine\\Mt19937
    -   [Random\\Engine\\Mt19937::\_\_construct](random-engine-mt19937.construct.md) \- Створює новий об'єкт двигуна Mt19937
    -   [Random\\Engine\\Mt19937::\_\_debugInfo](random-engine-mt19937.debuginfo.md) \- Повертає внутрішній стан двигуна
    -   [Random\\Engine\\Mt19937::generate](random-engine-mt19937.generate.md)— Створює 32 біти випадкової послідовності
    -   [Random\\Engine\\Mt19937::\_\_serialize](random-engine-mt19937.serialize.md)— Серіалізує об'єкт Mt19937
    -   [Random\\Engine\\Mt19937::\_\_unserialize](random-engine-mt19937.unserialize.md) \- Десеріалізує параметр data в об'єкт Mt19937
-   [Random\\Engine\\PcgOneseq128XslRr64](class.random-engine-pcgoneseq128xslrr64.md) \- Клас Random\\Engine\\PcgOneseq128XslRr64
    -   [Random\\Engine\\PcgOneseq128XslRr64::\_\_construct](random-engine-pcgoneseq128xslrr64.construct.md) \- Створює новий двигун PCG Oneseq 128 XSL RR 64
    -   [Random\\Engine\\PcgOneseq128XslRr64::\_\_debugInfo](random-engine-pcgoneseq128xslrr64.debuginfo.md) \- Повертає внутрішній стан двигуна
    -   [Random\\Engine\\PcgOneseq128XslRr64::generate](random-engine-pcgoneseq128xslrr64.generate.md)— Створює 64 біти випадкової послідовності
    -   [Random\\Engine\\PcgOneseq128XslRr64::jump](random-engine-pcgoneseq128xslrr64.jump.md) \- Ефективне переміщення двигуна вперед на кілька кроків
    -   [Random\\Engine\\PcgOneseq128XslRr64::\_\_serialize](random-engine-pcgoneseq128xslrr64.serialize.md)— Серіалізує об'єкт PcgOneseq128XslRr64
    -   [Random\\Engine\\PcgOneseq128XslRr64::\_\_unserialize](random-engine-pcgoneseq128xslrr64.unserialize.md)— Десеріалізує параметр data в об'єкт PcgOneseq128XslRr64
-   [Random\\Engine\\Xoshiro256StarStar](class.random-engine-xoshiro256starstar.md) \- Клас Random\\Engine\\Xoshiro256StarStar
    -   [Random\\Engine\\Xoshiro256StarStar::\_\_construct](random-engine-xoshiro256starstar.construct.md) \- Створює новий об'єкт двигуна xoshiro256\*\*
    -   [Random\\Engine\\Xoshiro256StarStar::\_\_debugInfo](random-engine-xoshiro256starstar.debuginfo.md) \- Повертає внутрішній стан двигуна
    -   [Random\\Engine\\Xoshiro256StarStar::generate](random-engine-xoshiro256starstar.generate.md)— Генерує 64 біти випадкової послідовності
    -   [Random\\Engine\\Xoshiro256StarStar::jump](random-engine-xoshiro256starstar.jump.md) \- Ефективно переміщає двигун вперед на 2^128 кроків
    -   [Random\\Engine\\Xoshiro256StarStar::jumpLong](random-engine-xoshiro256starstar.jumplong.md) \- Ефективно переміщає двигун вперед на 2^192 кроки
    -   [Random\\Engine\\Xoshiro256StarStar::\_\_serialize](random-engine-xoshiro256starstar.serialize.md) \- Серіалізує об'єкт Xoshiro256StarStar
    -   [Random\\Engine\\Xoshiro256StarStar::\_\_unserialize](random-engine-xoshiro256starstar.unserialize.md)— Десеріалізує параметр data в об'єкті Xoshiro256StarStar
-   [Random\\RandomError](class.random-randomerror.md) \- Клас Random\\RandomError
-   [Random\\BrokenRandomEngineError](class.random-brokenrandomengineerror.md) \- Клас Random\\BrokenRandomEngineError
-   [Random\\RandomException](class.random-randomexception.md) \- Клас Random\\RandomException
