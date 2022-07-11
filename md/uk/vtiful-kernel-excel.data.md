- [« Vtiful\Kernel\Excel::\_\_construct](vtiful-kernel-excel.construct.md)
- [Vtiful\Kernel\Excel::fileName »](vtiful-kernel-excel.filename.md)

- [PHP Manual](index.md)
- [Vtiful\Kernel\Excel](class.vtiful-kernel-excel.md)
- Записати дані

# Vtiful\Kernel\Excel::data

(PECL xlswriter \>= 1.2.1)

Vtiful\Kernel\Excel::data — Записати дані

### Опис

public **Vtiful\Kernel\Excel::data**(array `$data`)

Записати дані до таблиці.

### Список параметрів

`data`
Дані листа

### Значення, що повертаються

Примірник [Vtiful\Kernel\Excel](class.vtiful-kernel-excel.md)

### Приклади

**Приклад #1 Приклад використання**

` <?php$config = [   'path' => './tests'];$fileObject  = new \Vtiful\Kernel\Excel($config);$file = $fileObject->fileName('tutorial.xlsx', 'sheet_one')   ->header(['name', 'age'])    ->data([      ['viest', 23],      ['wjx', 23], |
