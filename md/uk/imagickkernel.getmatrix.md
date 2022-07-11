- [« ImagickKernel::fromMatrix](imagickkernel.frommatrix.md)
- [ImagickKernel::scale »](imagickkernel.scale.md)

- [PHP Manual](index.md)
- [ImagickKernel](class.imagickkernel.md)
- Опис

# ImagickKernel::getMatrix

(PECL imagick \>= 3.3.0)

ImagickKernel::getMatrix — Опис

### Опис

public **ImagickKernel::getMatrix**(): array

Отримати 2d матрицю значень, що використовуються у цьому ядрі. Елементи
є або числом з плаваючою точкою для використовуваних елементів, або
'false', якщо елемент має бути пропущений.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Матриця (2d масив) значень, що становлять ядро.

### Приклади

**Приклад #1 Приклад використання **ImagickKernel::getMatrix()****

` <?phpfunction renderKernelTable($matrix) {   $output = "<table class='infoTable'>"; foreach ($matrix as $row) {        $output .= "<tr>"; foreach ($row as $cell) {            $output .= "<td style='text-align:left'>"; if ($cell === false) {                $output .= "false"; }|||||||||||| }             $output .= "</td>"; }        $output .= "</tr>"; }   $output .= "</table>"; return $output;}   $output = "Ім'я вбудованого ядра 'ring' з параметрами '2,3.5':<br/>"; $kernel= \ImagickKernel::fromBuiltIn(        \Imagick::KERNEL_RING,        "2,3.5"    ); $matrix==$kernel->getMatrix(); $output.==renderKernelTable($matrix); echo $output;?> `
