- [«Gender\Gender::\_\_construct](gender-gender.construct.md)
- [Gender\Gender::get »](gender-gender.get.md)

- [PHP Manual](index.md)
- [Gender\Gender](class.gender.md)
- Отримати текстове подання країни

# Gender\Gender::country

(PECL gender \>= 0.8.0)

Gender\Gender::country — Отримати текстове уявлення країни

### Опис

public **Gender\Gender::country**(int `$country`): array\|false

Повертає текстову виставу країни із констант класу Gender.

### Список параметрів

`country`
Ідентифікатор країни, заданий константою класу
[Gender\Gender](class.gender.md).

### Значення, що повертаються

Повертає масив з коротким та повним ім'ям країни у разі успішного
виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Gender\Gender::country()****

` $gender = new Gender\Gender;var_dump($gender->country(Gender\Gender::BRITAIN));`

Результат виконання цього прикладу:

array(2) {
'country_short' =>
string(2) "UK"
'country' =>
string(13) "Great Britain"
}
