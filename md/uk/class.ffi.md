---
navigation:
  - ffi.examples-complete.html: « Комплексний приклад PHP/FFI/preloading
  - ffi.addr.md: 'FFI::addr »'
  - index.md: PHP Manual
  - book.ffi.md: FFI
title: Основний інтерфейс до коду та даних C
---
# Основний інтерфейс до коду та даних C

(PHP 7> = 7.4.0, PHP 8)

## Вступ

Об'єкти цього класу створюються фабричними методами [FFI::cdef()](ffi.cdef.md) [FFI::load()](ffi.load.md) і [FFI::scope()](ffi.scope.md). Оголошені змінні C доступні як властивості екземпляра FFI, а функції як його методи. Оголошені типи C можна використовувати для створення структур даних за допомогою [FFI::new()](ffi.new.md) і [FFI::type()](ffi.type.md)

Розбір оголошень FFI і завантаження бібліотеки, що розділяється, може зайняти значний час. Немає сенсу робити це для кожного HTTP-запиту в оточенні Web. Проте можна перезавантажити оголошення FFI та бібліотеки під час старту PHP та інстанціювати об'єкти FFI за потребою. Заголовні файли можуть бути розширені спеціальними оголошеннями `FFI_SCOPE` (наприклад, `#define FFI_SCOPE "foo"”"`; скоуп за замовчуванням "C") і завантажені за допомогою [FFI::load()](ffi.load.md) під час завантаження. Це призведе до створення постійних прив'язок, які будуть доступні для всіх запитів через [FFI::scope()](ffi.scope.md). Докладніше читайте на сторінці [Прості приклади використання FFI](ffi.examples-complete.md)

У той самий скоуп можна завантажити кілька заголовних файлів.

## Огляд класів

```classsynopsis

     
    

    
     
      final
      class FFI
     
     {

    /* Методы */
    
   public static addr(FFI\CData &$ptr): FFI\CData
public static alignof(FFI\CData|FFI\CType &$ptr): int
public static arrayType(FFI\CType $type, array $dimensions): FFI\CType
public static cast(FFI\CType|string $type, FFI\CData|int|float|bool|null &$ptr): ?FFI\CData
public cast(FFI\CType|string $type, FFI\CData|int|float|bool|null &$ptr): ?FFI\CData
public static cdef(string $code = "", ?string $lib = null): FFI
public static free(FFI\CData &$ptr): void
public static isNull(FFI\CData &$ptr): bool
public static load(string $filename): ?FFI
public static memcmp(string|FFI\CData &$ptr1, string|FFI\CData &$ptr2, int $size): int
public static memcpy(FFI\CData &$to, FFI\CData|string &$from, int $size): void
public static memset(FFI\CData &$ptr, int $value, int $size): void
public static new(FFI\CType|string $type, bool $owned = true, bool $persistent = false): ?FFI\CData
public new(FFI\CType|string $type, bool $owned = true, bool $persistent = false): ?FFI\CData
public static scope(string $name): FFI
public static sizeof(FFI\CData|FFI\CType &$ptr): int
public static string(FFI\CData &$ptr, ?int $size = null): string
public static type(string $type): ?FFI\CType
public type(string $type): ?FFI\CType
public static typeof(FFI\CData &$ptr): FFI\CType

   }
```

## Зміст

-   [FFI::addr](ffi.addr.md) — Створює некерований покажчик даних C
-   [FFI::alignof](ffi.alignof.md) - Повертає величину вирівнювання
-   [FFI::arrayType](ffi.arraytype.md) — Динамічно конструює новий тип масиву
-   [FFI::cast](ffi.cast.md) — Здійснює перетворення типу C
-   [FFI::cdef](ffi.cdef.md) — Створює новий об'єкт FFI
-   [FFI::free](ffi.free.md) — Вивільняє некеровану структуру даних
-   [FFI::isNull](ffi.isnull.md) — Перевіряє, чи є FFICData нульовим покажчиком
-   [FFI::load](ffi.load.md) — Завантажити декларації C із заголовного файлу
-   [FFI::memcmp](ffi.memcmp.md) — Порівнює дві області пам'яті
-   [FFI::memcpy](ffi.memcpy.md) — Копіює вміст однієї області пам'яті в іншу
-   [FFI::memset](ffi.memset.md) — Заповнити область пам'яті
-   [FFI::new](ffi.new.md) - Створює структуру даних C
-   [FFI::scope](ffi.scope.md) — Інстанціює об'єкт FFI відповідно до декларації С, розібраної на етапі передзавантаження
-   [FFI::sizeof](ffi.sizeof.md) — Повертає розмір даних або типу C
-   [FFI::string](ffi.string.md) — Створює рядок PHP із області пам'яті
-   [FFI::type](ffi.type.md) — Створює об'єкт FFICType із декларації С
-   [FFI::typeof](ffi.typeof.md) — Отримує FFICType для FFICData
