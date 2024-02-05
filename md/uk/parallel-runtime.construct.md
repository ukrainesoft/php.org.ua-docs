---
navigation:
  - class.parallel-runtime.md: « parallel\\Runtime
  - parallel-runtime.run.md: 'parallel\\Runtime::run »'
  - index.md: PHP Manual
  - class.parallel-runtime.md: parallel\\Runtime
title: 'parallel\\Runtime::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# parallel\\Runtime::\_\_construct

(0.8.0)

parallel\\Runtime::\_\_construct - Конструктор класу Runtime

### Опис

public**parallel\\Runtime::\_\_construct**()

Створює нове виконання без початкового завантаження.

public**parallel\\Runtime::\_\_construct**(string`$bootstrap`) .

Створює нове середовище виконання з початковим завантаженням.

### Список параметрів

`bootstrap`

Розташування файлу початкового завантаження зазвичай це автозавантажувач.

### Помилки

**Увага**

Викидає parallel\\Runtime\\Error, якщо потік не може бути створений.

**Увага**

Викидає parallel\\Runtime\\Bootstrap, якщо початкове завантаження завершилося з помилкою.
