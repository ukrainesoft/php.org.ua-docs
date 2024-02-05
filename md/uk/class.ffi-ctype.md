---
navigation:
  - class.ffi-cdata.md: « FFI\\CData
  - ffi-ctype.getalignment.md: 'FFI\\CType::getAlignment »'
  - index.md: PHP Manual
  - book.ffi.md: FFI
title: Доступ до типів C
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Доступ до типів C

(PHP 7 >= 7.4.0, PHP 8)

## Вступ

## Огляд класів

```classsynopsis

    
     final
     class FFI\CType
     {

    /* Константы */
    
     public
     const
     int
      TYPE_VOID;

    public
     const
     int
      TYPE_FLOAT;

    public
     const
     int
      TYPE_DOUBLE;

    public
     const
     int
      TYPE_LONGDOUBLE;

    public
     const
     int
      TYPE_UINT8;

    public
     const
     int
      TYPE_SINT8;

    public
     const
     int
      TYPE_UINT16;

    public
     const
     int
      TYPE_SINT16;

    public
     const
     int
      TYPE_UINT32;

    public
     const
     int
      TYPE_SINT32;

    public
     const
     int
      TYPE_UINT64;

    public
     const
     int
      TYPE_SINT64;

    public
     const
     int
      TYPE_ENUM;

    public
     const
     int
      TYPE_BOOL;

    public
     const
     int
      TYPE_CHAR;

    public
     const
     int
      TYPE_POINTER;

    public
     const
     int
      TYPE_FUNC;

    public
     const
     int
      TYPE_ARRAY;

    public
     const
     int
      TYPE_STRUCT;

    public
     const
     int
      ATTR_CONST;

    public
     const
     int
      ATTR_INCOMPLETE_TAG;

    public
     const
     int
      ATTR_VARIADIC;

    public
     const
     int
      ATTR_INCOMPLETE_ARRAY;

    public
     const
     int
      ATTR_VLA;

    public
     const
     int
      ATTR_UNION;

    public
     const
     int
      ATTR_PACKED;

    public
     const
     int
      ATTR_MS_STRUCT;

    public
     const
     int
      ATTR_GCC_STRUCT;

    public
     const
     int
      ABI_DEFAULT;

    public
     const
     int
      ABI_CDECL;

    public
     const
     int
      ABI_FASTCALL;

    public
     const
     int
      ABI_THISCALL;

    public
     const
     int
      ABI_STDCALL;

    public
     const
     int
      ABI_PASCAL;

    public
     const
     int
      ABI_REGISTER;

    public
     const
     int
      ABI_MS;

    public
     const
     int
      ABI_SYSV;

    public
     const
     int
      ABI_VECTORCALL;


    /* Методы */
    
   public getAlignment(): int
public getArrayElementType(): FFI\CType
public getArrayLength(): int
public getAttributes(): int
public getEnumKind(): int
public getFuncABI(): int
public getFuncParameterCount(): int
public getFuncParameterType(int $index): FFI\CType
public getFuncReturnType(): FFI\CType
public getKind(): int
public getName(): string
public getPointerType(): FFI\CType
public getSize(): int
public getStructFieldNames(): array
public getStructFieldOffset(string $name): int
public getStructFieldType(string $name): FFI\CType

   }
```

## Обумовлені константи

**`FFI\CType::TYPE_VOID`**

**`FFI\CType::TYPE_FLOAT`**

**`FFI\CType::TYPE_DOUBLE`**

**`FFI\CType::TYPE_LONGDOUBLE`**

**`FFI\CType::TYPE_UINT8`**

**`FFI\CType::TYPE_SINT8`**

**`FFI\CType::TYPE_UINT16`**

**`FFI\CType::TYPE_SINT16`**

**`FFI\CType::TYPE_UINT32`**

**`FFI\CType::TYPE_SINT32`**

**`FFI\CType::TYPE_UINT64`**

**`FFI\CType::TYPE_SINT64`**

**`FFI\CType::TYPE_ENUM`**

**`FFI\CType::TYPE_BOOL`**

**`FFI\CType::TYPE_CHAR`**

**`FFI\CType::TYPE_POINTER`**

**`FFI\CType::TYPE_FUNC`**

**`FFI\CType::TYPE_ARRAY`**

**`FFI\CType::TYPE_STRUCT`**

**`FFI\CType::ATTR_CONST`**

**`FFI\CType::ATTR_INCOMPLETE_TAG`**

**`FFI\CType::ATTR_VARIADIC`**

**`FFI\CType::ATTR_INCOMPLETE_ARRAY`**

**`FFI\CType::ATTR_VLA`**

**`FFI\CType::ATTR_UNION`**

**`FFI\CType::ATTR_PACKED`**

**`FFI\CType::ATTR_MS_STRUCT`**

**`FFI\CType::ATTR_GCC_STRUCT`**

**`FFI\CType::ABI_DEFAULT`**

**`FFI\CType::ABI_CDECL`**

**`FFI\CType::ABI_FASTCALL`**

**`FFI\CType::ABI_THISCALL`**

**`FFI\CType::ABI_STDCALL`**

**`FFI\CType::ABI_PASCAL`**

**`FFI\CType::ABI_REGISTER`**

**`FFI\CType::ABI_MS`**

**`FFI\CType::ABI_SYSV`**

**`FFI\CType::ABI_VECTORCALL`**

## Зміст

-   [FFI\\CType::getAlignment](ffi-ctype.getalignment.md) \- Опис
-   [FFI\\CType::getArrayElementType](ffi-ctype.getarrayelementtype.md) \- Опис
-   [FFI\\CType::getArrayLength](ffi-ctype.getarraylength.md) \- Опис
-   [FFI\\CType::getAttributes](ffi-ctype.getattributes.md) \- Опис
-   [FFI\\CType::getEnumKind](ffi-ctype.getenumkind.md) \- Опис
-   [FFI\\CType::getFuncABI](ffi-ctype.getfuncabi.md) \- Опис
-   [FFI\\CType::getFuncParameterCount](ffi-ctype.getfuncparametercount.md) \- Опис
-   [FFI\\CType::getFuncParameterType](ffi-ctype.getfuncparametertype.md) \- Опис
-   [FFI\\CType::getFuncReturnType](ffi-ctype.getfuncreturntype.md) \- Опис
-   [FFI\\CType::getKind](ffi-ctype.getkind.md) \- Опис
-   [FFI\\CType::getName](ffi-ctype.getname.md) \- Опис
-   [FFI\\CType::getPointerType](ffi-ctype.getpointertype.md) \- Опис
-   [FFI\\CType::getSize](ffi-ctype.getsize.md) \- Опис
-   [FFI\\CType::getStructFieldNames](ffi-ctype.getstructfieldnames.md) \- Опис
-   [FFI\\CType::getStructFieldOffset](ffi-ctype.getstructfieldoffset.md) \- Опис
-   [FFI\\CType::getStructFieldType](ffi-ctype.getstructfieldtype.md) \- Опис
