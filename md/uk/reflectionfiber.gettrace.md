Отримує зворотне трасування поточної точки виконання

-   [« ReflectionFiber::getFiber](reflectionfiber.getfiber.html)
    
-   [ReflectionIntersectionType »](class.reflectionintersectiontype.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionFiber](class.reflectionfiber.html)
    
-   Отримує зворотне трасування поточної точки виконання
    

# ReflectionFiber::getTrace

(PHP 8> = 8.1.0)

ReflectionFiber::getTrace — Отримує зворотне трасування поточної точки виконання

### Опис

```methodsynopsis
public ReflectionFiber::getTrace(int $options = DEBUG_BACKTRACE_PROVIDE_OBJECT): array
```

Отримує зворотне трасування поточної точки виконання відображеного класу [Fiber](class.fiber.html)

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