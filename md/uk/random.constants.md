---
navigation:
  - random.resources.md: « Типи ресурсів
  - random.examples.md: Приклади »
  - index.md: PHP Manual
  - book.random.md: Random
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи завжди доступні як частина ядра PHP.

**`MT_RAND_MT19937`**(int)

Вказує, що правильна реалізація [» Mt19937](http://www.math.sci.hiroshima-u.ac.jp/m-mat/MT/ARTICLES/mt.pdf) (Mersenne Twister) використовуватиметься алгоритмом при створенні екземпляра [Random\\Engine\\Mt19937](class.random-engine-mt19937.md)с помощью метода[Random\\Engine\\Mt19937::\_\_construct()](random-engine-mt19937.construct.md)или при загрузке глобального Mersenne Twister с помощью функции[mt\_srand()](function.mt-srand.md)

**`MT_RAND_PHP`**(int)

Вказує, що при створенні екземпляра [Random\\Engine\\Mt19937](class.random-engine-mt19937.md)с помощью метода[Random\\Engine\\Mt19937::\_\_construct()](random-engine-mt19937.construct.md)или при загрузке глобального Mersenne Twister с помощью функции[mt\_srand()](function.mt-srand.md) алгоритм використовуватиме некоректну реалізацію Mersenne Twister. Некоректна реалізація доступна для зворотної сумісності за допомогою функції [mt\_srand()](function.mt-srand.md) до версії PHP 7.1.0.

**Увага**

Ця функціональність оголошена *застарілої* починаючи з PHP 8.3.0 і її украй не рекомендується використовувати.
