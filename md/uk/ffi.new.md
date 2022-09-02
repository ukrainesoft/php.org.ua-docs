---
navigation:
  - ffi.memset.md: '« FFI::memset'
  - ffi.scope.md: 'FFI::scope »'
  - index.md: PHP Manual
  - class.ffi.md: FFI
title: 'FFI::new'
---
# FFI::new

(PHP 7> = 7.4.0, PHP 8)

FFI::new — Створює структуру даних C

### Опис

```methodsynopsis
public static FFI::new(FFI\CType|string $type, bool $owned = true, bool $persistent = false): ?FFI\CData
```

```methodsynopsis
public FFI::new(FFI\CType|string $type, bool $owned = true, bool $persistent = false): ?FFI\CData
```

Створює нативну структуру даних заданого типу. При статичному виклику даного методу необхідно використовувати лише визначені імена типів С (такі як `int` `char`, і т.д.); при виклик як метод об'єкта, припустимо будь-який тип оголошений йому.

### Список параметрів

`type`

`type` - коректна декларація типу С, наприклад, string або заздалегідь створений об'єкт класу [FFICType](class.ffi-ctype.md)

`owned`

Чи створювати керовані чи некеровані дані. Керовані дані живуть у зв'язці з повернутим об'єктом [FFICData](class.ffi-cdata.md) і вивільняється, коли стандартний підрахунок посилань PHP або GC (збирач сміття) звільнять останнє посилання на цей об'єкт. Некеровані дані необхідно вивільняти вручну за допомогою [FFI::free()](ffi.free.md)

`persistent`

Чи мати дані на постійній основі до системної купи (heap) (використовуючи **malloc()**), або в купі запиту PHP (використовуючи **emalloc()**

### Значення, що повертаються

Повертає новий об'єкт [FFICData](class.ffi-cdata.md) або **`null`** у разі виникнення помилки.
