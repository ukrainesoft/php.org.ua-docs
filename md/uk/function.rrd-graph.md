- [«rrd_first](function.rrd-first.md)
- [rrd_info »](function.rrd-info.md)

- [PHP Manual](index.md)
- [Функції RRD](ref.rrd.md)
- Створює зображення з даних

#rrd_graph

(PECL rrd \>= 0.9.0)

rrd_graph — Створює зображення з даних

### Опис

**rrd_graph**(string `$filename`, array `$options`): array

Створює зображення для певних даних із RRD-файлу.

### Список параметрів

`filename`
Назва файлу для виведення графіка. Це, як правило, закінчується або
`.png`, `.svg` або `.eps`, залежно від потрібного формату виведення.

`options`
Опції для створення зображення. Дивіться сторінку керівництва для
команди rrd graph для отримання можливих варіантів. Усі опції
(Визначення даних, визначення змінних і т.д.) дозволені.

### Значення, що повертаються

Повертається масив з інформацією про згенероване зображення або
**`false`** у разі виникнення помилки.
