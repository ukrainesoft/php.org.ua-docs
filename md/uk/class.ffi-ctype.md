---
navigation:
  - class.ffi-cdata.md: « FFICData
  - ffi-ctype.getalignment.md: 'FFICType::getAlignment »'
  - index.md: PHP Manual
  - book.ffi.md: FFI
title: Доступ до типів C
---
# Доступ до типів C

(PHP 7> = 7.4.0, PHP 8)

## Вступ

## Огляд класів

```classsynopsis

     
    

    
     
      final
      class FFI\CType
     
     {

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

## Зміст

-   [FFICType::getAlignment](ffi-ctype.getalignment.md) - Опис
-   [FFICType::getArrayElementType](ffi-ctype.getarrayelementtype.md) - Опис
-   [FFICType::getArrayLength](ffi-ctype.getarraylength.md) - Опис
-   [FFICType::getAttributes](ffi-ctype.getattributes.md) - Опис
-   [FFICType::getEnumKind](ffi-ctype.getenumkind.md) - Опис
-   [FFICType::getFuncABI](ffi-ctype.getfuncabi.md) - Опис
-   [FFICType::getFuncParameterCount](ffi-ctype.getfuncparametercount.md) - Опис
-   [FFICType::getFuncParameterType](ffi-ctype.getfuncparametertype.md) - Опис
-   [FFICType::getFuncReturnType](ffi-ctype.getfuncreturntype.md) - Опис
-   [FFICType::getKind](ffi-ctype.getkind.md) - Опис
-   [FFICType::getName](ffi-ctype.getname.md) - Опис
-   [FFICType::getPointerType](ffi-ctype.getpointertype.md) - Опис
-   [FFICType::getSize](ffi-ctype.getsize.md) - Опис
-   [FFICType::getStructFieldNames](ffi-ctype.getstructfieldnames.md) - Опис
-   [FFICType::getStructFieldOffset](ffi-ctype.getstructfieldoffset.md) - Опис
-   [FFICType::getStructFieldType](ffi-ctype.getstructfieldtype.md) - Опис
