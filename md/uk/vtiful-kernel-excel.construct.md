- [« Vtiful\Kernel\Excel::constMemory](vtiful-kernel-excel.constMemory.md)
- [Vtiful\Kernel\Excel::data »](vtiful-kernel-excel.data.md)

- [PHP Manual](index.md)
- [Vtiful\Kernel\Excel](class.vtiful-kernel-excel.md)
- Конструктор

# Vtiful\Kernel\Excel::\_\_construct

(PECL xlswriter \>= 1.2.1)

Vtiful\Kernel\Excel::\_\_construct - Конструктор

### Опис

public **Vtiful\Kernel\Excel::\_\_construct**(array `$config`)

Конструктор [Vtiful\Kernel\Excel](class.vtiful-kernel-excel.md),
створити екземпляр.

### Список параметрів

`config`
Конфігурація експорту файлу XLSX

### Приклади

**Приклад #1 Приклад використання**

` <?php$config = [  'path' => '/home/viest'];$excelObject = new \Vtiful\Kernel\Excel($config);?> `
