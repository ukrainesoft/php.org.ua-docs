- [« Vtiful\Kernel\Excel::getHandle](vtiful-kernel-excel.getHandle.md)
- [Vtiful\Kernel\Excel::insertFormula »](vtiful-kernel-excel.insertFormula.md)

- [PHP Manual](index.md)
- [Vtiful\Kernel\Excel](class.vtiful-kernel-excel.md)
- Записати заголовок

# Vtiful\Kernel\Excel::header

(PECL xlswriter \>= 1.2.1)

Vtiful\Kernel\Excel::header — Записати заголовок

### Опис

public **Vtiful\Kernel\Excel::header**(array `$headerData`)

Написати заголовок на аркуші.

### Список параметрів

`headerData`
Дані заголовка аркуша

### Значення, що повертаються

Примірник [Vtiful\Kernel\Excel](class.vtiful-kernel-excel.md)

### Приклади

**Приклад #1 Приклад використання**

` <?php$config = [   'path' => './tests'];$fileObject  = new \Vtiful\Kernel\Excel($config);$file = $fileObject->fileName('tutorial.xlsx', 'sheet_one')    ->header(['name', 'age']);?> `
