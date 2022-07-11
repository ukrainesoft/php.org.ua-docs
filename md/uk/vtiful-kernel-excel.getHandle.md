- [« Vtiful\Kernel\Excel::fileName](vtiful-kernel-excel.filename.md)
- [Vtiful\Kernel\Excel::header »](vtiful-kernel-excel.header.md)

- [PHP Manual](index.md)
- [Vtiful\Kernel\Excel](class.vtiful-kernel-excel.md)
- Отримати дескриптор

# Vtiful\Kernel\Excel::getHandle

(PECL xlswriter \>= 1.2.1)

Vtiful\Kernel\Excel::getHandle — Отримати дескриптор

### Опис

public **Vtiful\Kernel\Excel::getHandle**()

Отримати дескриптор текстового ресурсу xlsx.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ресурс

### Приклади

**Приклад #1 Приклад використання**

` <?php$config = [   'path' => './tests'];$fileObject  = new \Vtiful\Kernel\Excel($config);$file = $fileObject->fileName('tutorial.xlsx', 'sheet_one')    ->header(['name', 'age']);$handle==$file->getHandle();?> `
