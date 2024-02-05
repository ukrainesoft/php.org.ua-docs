---
navigation:
  - reflectionfiber.getfiber.md: '« ReflectionFiber::getFiber'
  - class.reflectionintersectiontype.md: ReflectionIntersectionType »
  - index.md: PHP Manual
  - class.reflectionfiber.md: ReflectionFiber
title: 'ReflectionFiber::getTrace'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionFiber::getTrace

(PHP 8 >= 8.1.0)

ReflectionFiber::getTrace — Отримує зворотне трасування поточної точки виконання

### Опис

```methodsynopsis
public ReflectionFiber::getTrace(int $options = DEBUG_BACKTRACE_PROVIDE_OBJECT): array
```

Отримує зворотне трасування поточної точки виконання відображеного класу [Fiber](class.fiber.md)

### Список параметрів

`options`

Значение`options` може бути будь-яким із наступних прапорів: the following flags.

**Доступні параметри**

| Параметр | Опис |
| --- | --- |
| **`DEBUG_BACKTRACE_PROVIDE_OBJECT`** | За замовчуванням. |
| **`DEBUG_BACKTRACE_IGNORE_ARGS`** | Не включати інформацію про аргумент для функцій трасування стека. |

### Значення, що повертаються

Відстежує поточну точку виконання файбера.
