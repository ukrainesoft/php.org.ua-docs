---
navigation:
  - xlswriter.constants.md: « Зумовлені константи
  - vtiful-kernel-excel.addSheet.md: 'Vtiful\\Kernel\\Excel::addSheet »'
  - index.md: PHP Manual
  - book.xlswriter.md: XLSWriter
title: Клас Vtiful\\Kernel\\Excel
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Vtiful\\Kernel\\Excel

(PECL xlswriter >= 1.2.1)

## Вступ

Створює файли xlsx із заданими осередками

## Огляд класів

```classsynopsis


    
    
     
      class Vtiful\Kernel\Excel
     
     {
    

    /* Методы */
    
   public __construct(array $config)

    public addSheet(string $sheetName)
public autoFilter(string $scope)
public constMemory(string $fileName, string $sheetName = ?)
public data(array $data)
public fileName(string $fileName, string $sheetName = ?)
public getHandle()
public header(array $headerData)
public insertFormula(int $row, int $column, string $formula)
public insertImage(int $row, int $column, string $localImagePath)
public insertText(    int $row,    int $column,    int|float|string $data,    string $format = ?)
public mergeCells(string $scope, string $data)
public output()
public setColumn(string $range, float $width, resource $format = ?)
public setRow(string $range, float $height, resource $format = ?)


   }
```

## Зміст

-   [Vtiful\\Kernel\\Excel::addSheet](vtiful-kernel-excel.addSheet.md) \- Додати лист
-   [Vtiful\\Kernel\\Excel::autoFilter](vtiful-kernel-excel.autoFilter.md) \- Додати автофільтр
-   [Vtiful\\Kernel\\Excel::constMemory](vtiful-kernel-excel.constMemory.md) \- Кількість пам'яті
-   [Vtiful\\Kernel\\Excel::\_\_construct](vtiful-kernel-excel.construct.md) \- Конструктор
-   [Vtiful\\Kernel\\Excel::data](vtiful-kernel-excel.data.md) \- Записати дані
-   [Vtiful\\Kernel\\Excel::fileName](vtiful-kernel-excel.filename.md)— Створити назву файлу
-   [Vtiful\\Kernel\\Excel::getHandle](vtiful-kernel-excel.getHandle.md) \- Отримати дескриптор
-   [Vtiful\\Kernel\\Excel::header](vtiful-kernel-excel.header.md) \- Записати заголовок
-   [Vtiful\\Kernel\\Excel::insertFormula](vtiful-kernel-excel.insertFormula.md) \- Вставити формулу розрахунку
-   [Vtiful\\Kernel\\Excel::insertImage](vtiful-kernel-excel.insertImage.md)— Вставити зображення
-   [Vtiful\\Kernel\\Excel::insertText](vtiful-kernel-excel.insertText.md)— Вставити текст
-   [Vtiful\\Kernel\\Excel::mergeCells](vtiful-kernel-excel.mergeCells.md) \- Об'єднати комірки
-   [Vtiful\\Kernel\\Excel::output](vtiful-kernel-excel.output.md) \- Висновок
-   [Vtiful\\Kernel\\Excel::setColumn](vtiful-kernel-excel.setColumn.md) \- Встановити стовпець
-   [Vtiful\\Kernel\\Excel::setRow](vtiful-kernel-excel.setRow.md) \- Встановити рядок
