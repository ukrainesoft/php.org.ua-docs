---
navigation:
  - reflectionfiber.getfiber.md: '« ReflectionFiber::getFiber'
  - class.reflectionintersectiontype.md: ReflectionIntersectionType »
  - index.md: PHP Manual
  - class.reflectionfiber.md: ReflectionFiber
title: 'ReflectionFiber::getTrace'
---
# ReflectionFiber::getTrace

(PHP 8> = 8.1.0)

ReflectionFiber::getTrace — Отримує зворотне трасування поточної точки виконання

### Опис

```methodsynopsis
public ReflectionFiber::getTrace(int $options = DEBUG_BACKTRACE_PROVIDE_OBJECT): array
```

Отримує зворотне трасування поточної точки виконання відображеного класу [Fiber](class.fiber.md)

### Список параметрів

`options`

Значення `options` може бути будь-яким із наступних прапорів: the following flags.

**Доступні параметри**

| Параметр | Описание |
| --- | --- |
| **`DEBUG_BACKTRACE_PROVIDE_OBJECT`** | За замовчуванням. |
| **`DEBUG_BACKTRACE_IGNORE_ARGS`** | Не включати інформацію про аргумент для функцій трасування стека. |

### Значення, що повертаються

Відстежує поточну точку виконання файбера.
