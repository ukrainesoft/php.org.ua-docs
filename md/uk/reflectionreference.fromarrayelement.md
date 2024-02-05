---
navigation:
  - reflectionreference.construct.md: '« ReflectionReference::\_\_construct'
  - reflectionreference.getid.md: 'ReflectionReference::getId »'
  - index.md: PHP Manual
  - class.reflectionreference.md: ReflectionReference
title: 'ReflectionReference::fromArrayElement'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionReference::fromArrayElement

(PHP 7 >= 7.4.0, PHP 8)

Reflection Reference::fromArrayElement — Створює Reflection Reference із елемента масиву

### Опис

```methodsynopsis
public static ReflectionReference::fromArrayElement(array $array, int|string $key): ?ReflectionReference
```

Створює [ReflectionReference](class.reflectionreference.md) елемент масиву.

### Список параметрів

`array`

Масив, що містить потенційне посилання.

`key`

Ключ; ціле число(int) чи рядок(string).

### Значення, що повертаються

Повертає екземпляр **ReflectionReference** якщо `$array[$key]` є посиланням, або **`null`** в іншому випадку.

### Помилки

Якщо `array` не є масивом, або `key` не є цілим числом (int) або рядком (string), буде викинуто виняток [TypeError](class.typeerror.md). Якщо `$array[$key]` не заданий, то буде викинуто виняток [ReflectionException](class.reflectionexception.md)
