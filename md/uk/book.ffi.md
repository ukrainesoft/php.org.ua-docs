Інтерфейс зовнішньої функції (Foreign Function Interface)

-   [« user\_error](function.user-error.html)
    
-   [Введение »](intro.ffi.html)
    
-   [PHP Manual](index.html)
    
-   [Изменение поведения PHP](refs.basic.php.html)
    
-   Інтерфейс зовнішньої функції (Foreign Function Interface)
    

# Інтерфейс зовнішньої функції (Foreign Function Interface)

-   [Введение](intro.ffi.html)
-   [Установка и настройка](ffi.setup.html)
    -   [Требования](ffi.requirements.html)
    -   [Установка](ffi.installation.html)
    -   [Настройка во время выполнения](ffi.configuration.html)
    -   [Типы ресурсов](ffi.resources.html)
-   [Предопределённые константы](ffi.constants.html)
-   [Примеры](ffi.examples.html)
    -   [Простые примеры использования FFI](ffi.examples-basic.html)
    -   [Callback-функции PHP](ffi.examples-callback.html)
    -   [Комплексный пример PHP/FFI/preloading](ffi.examples-complete.html)
-   [FFI](class.ffi.html) — Основний інтерфейс до коду та даних C
    -   [FFI::addr](ffi.addr.html) — Створює некерований покажчик даних C
    -   [FFI::alignof](ffi.alignof.html) - Повертає величину вирівнювання
    -   [FFI::arrayType](ffi.arraytype.html) — Динамічно конструює новий тип масиву
    -   [FFI::cast](ffi.cast.html) — Здійснює перетворення типу C
    -   [FFI::cdef](ffi.cdef.html) — Створює новий об'єкт FFI
    -   [FFI::free](ffi.free.html) — Вивільняє некеровану структуру даних
    -   [FFI::isNull](ffi.isnull.html) — Перевіряє, чи є FFICData нульовим покажчиком
    -   [FFI::load](ffi.load.html) — Завантажити декларації C із заголовного файлу
    -   [FFI::memcmp](ffi.memcmp.html) — Порівнює дві області пам'яті
    -   [FFI::memcpy](ffi.memcpy.html) — Копіює вміст однієї області пам'яті в іншу
    -   [FFI::memset](ffi.memset.html) — Заповнити область пам'яті
    -   [FFI::new](ffi.new.html) - Створює структуру даних C
    -   [FFI::scope](ffi.scope.html) — Інстанціює об'єкт FFI відповідно до декларації С, розібраної на етапі передзавантаження
    -   [FFI::sizeof](ffi.sizeof.html) — Повертає розмір даних або типу C
    -   [FFI::string](ffi.string.html) — Створює рядок PHP із області пам'яті
    -   [FFI::type](ffi.type.html) — Створює об'єкт FFICType із декларації С
    -   [FFI::typeof](ffi.typeof.html) — Отримує FFICType для FFICData
-   [FFI\\CData](class.ffi-cdata.html) — Доступ до даних C
-   [FFI\\CType](class.ffi-ctype.html) — Доступ до типів C
    -   [FFI\\CType::getAlignment](ffi-ctype.getalignment.html) - Опис
    -   [FFI\\CType::getArrayElementType](ffi-ctype.getarrayelementtype.html) - Опис
    -   [FFI\\CType::getArrayLength](ffi-ctype.getarraylength.html) - Опис
    -   [FFI\\CType::getAttributes](ffi-ctype.getattributes.html) - Опис
    -   [FFI\\CType::getEnumKind](ffi-ctype.getenumkind.html) - Опис
    -   [FFI\\CType::getFuncABI](ffi-ctype.getfuncabi.html) - Опис
    -   [FFI\\CType::getFuncParameterCount](ffi-ctype.getfuncparametercount.html) - Опис
    -   [FFI\\CType::getFuncParameterType](ffi-ctype.getfuncparametertype.html) - Опис
    -   [FFI\\CType::getFuncReturnType](ffi-ctype.getfuncreturntype.html) - Опис
    -   [FFI\\CType::getKind](ffi-ctype.getkind.html) - Опис
    -   [FFI\\CType::getName](ffi-ctype.getname.html) - Опис
    -   [FFI\\CType::getPointerType](ffi-ctype.getpointertype.html) - Опис
    -   [FFI\\CType::getSize](ffi-ctype.getsize.html) - Опис
    -   [FFI\\CType::getStructFieldNames](ffi-ctype.getstructfieldnames.html) - Опис
    -   [FFI\\CType::getStructFieldOffset](ffi-ctype.getstructfieldoffset.html) - Опис
    -   [FFI\\CType::getStructFieldType](ffi-ctype.getstructfieldtype.html) - Опис
-   [FFI\\Exception](class.ffi-exception.html) - Винятки FFI
-   [FFI\\ParserException](class.ffi-parserexception.html) - Виключення парсера FFI