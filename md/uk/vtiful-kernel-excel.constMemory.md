- [« Vtiful\Kernel\Excel::autoFilter](vtiful-kernel-excel.autoFilter.md)
- [Vtiful\Kernel\Excel::\_\_construct »](vtiful-kernel-excel.construct.md)

- [PHP Manual](index.md)
- [Vtiful\Kernel\Excel](class.vtiful-kernel-excel.md)
- Кількість пам'яті

# Vtiful\Kernel\Excel::constMemory

(PECL xlswriter \>= 1.2.1)

Vtiful\Kernel\Excel::constMemory — Кількість пам'яті

### Опис

public **Vtiful\Kernel\Excel::constMemory**(string `$fileName`, string
`$sheetName` = ?)

Запис великого файлу з використанням пам'яті.

### Список параметрів

`fileName`
Ім'я файлу XLSX

`sheetName`
Назва листа

### Значення, що повертаються

Примірник [Vtiful\Kernel\Excel](class.vtiful-kernel-excel.md)

### Приклади

**Приклад #1 Приклад використання**

` <?php$config = [ 'path' => '/home/viest'];$fileObject = new \Vtiful\Kernel\Excel($config);$file = $instance->constMemory('tutorial.xlsx'' , 'sheet');?> `
