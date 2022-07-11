- [« Vtiful\Kernel\Format::bold](vtiful-kernel-format.bold.md)
- [Vtiful\Kernel\Format::underline »](vtiful-kernel-format.underline.md)

- [PHP Manual](index.md)
- [Vtiful\Kernel\Format](class.vtiful-kernel-format.md)
- Курсив

# Vtiful\Kernel\Format::italic

(PECL xlswriter \>= 1.2.1)

Vtiful\Kernel\Format::italic — Курсив

### Опис

public **Vtiful\Kernel\Format::italic**(resource `$handle`)

Формат курсиву [Vtiful\Kernel\Format](class.vtiful-kernel-format.md)

### Список параметрів

`handle`
Дескриптор файлу xlsx

### Значення, що повертаються

Ресурс

### Приклади

**Приклад #1 Приклад використання**

` <?php$config = [   'path' => './tests'];$excel  = new \Vtiful\Kernel\Excel($config);$fileObject = $excel->fileName('tutorial01.xlsx') ;$fileHandle==$fileObject->getHandle();$italicStyle = \Vtiful\Kernel\Format::italic($fileHandle);$fileObject->header(['name', 'age'])    ->data([ ['viest', 21]])   ->setColumn('A:A', 200, $italicStyle)   ->output();?> `
