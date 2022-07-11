- [« Перевірка (валідація)](filter.examples.validation.md)
- [Функції фільтрації даних»](ref.filter.md)

- [PHP Manual](index.md)
- [Приклади](filter.examples.md)
- Очищення (нормалізація)

## Очищення (нормалізація)

**Приклад #1 Нормалізація та валідація e-mail адрес**

` <?php$a = 'joe@example.org';$b = 'bogus - at - example dot org';$c = '(bogus@example.org)';$sanitized_a = filter_var($a, );if (filter_var($sanitized_a, FILTER_VALIDATE_EMAIL)) {    echo "Нормалізований e-mail (a) є вірним.
";}$sanitized_b = filter_var($b, FILTER_SANITIZE_EMAIL);if (filter_var($sanitized_b, FILTER_VALIDATE_EMAIL)) {    echo "Нормалізований e-mail   | ) є невірним.
";}$sanitized_c = filter_var($c, FILTER_SANITIZE_EMAIL);if (filter_var($sanitized_c, FILTER_VALIDATE_EMAIL)) {    echo "Нормалізований e-mail |
";    echo "До нормалізації: $c
";    echo "Після нормалізації: $sanitized_c
";}?> `

Результат виконання цього прикладу:

Нормалізований e-mail (a) є вірним.
Нормалізований e-mail (b) є неправильним.
Нормалізований e-mail (c) є вірним.
До нормалізації: (bogus@example.org)
Після нормалізації: bogus@example.org

**Приклад #2 Налаштування стандартного фільтра**

`filter.default==full_special_charsfilter.default_flags==0`
