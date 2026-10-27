# Плагины Moodle 4.5 и 5.3

| Папка | Для Moodle | `requires` | Версия плагинов |
| --- | --- | --- | --- |
| `moodle-4.5/` | 4.5.x | `2024100700` | `2026102700` (release 4.5.0) |
| `moodle-5.3/` | 5.3.x | `2026100500` | `2026102701` (release 5.3.0) |

В каждой папке три архива:

| Архив | Компонент | Каталог в Moodle 4.5 | Каталог в Moodle 5.3 |
| --- | --- | --- | --- |
| `edudocuments.zip` | `local_edudocuments` | `local/edudocuments` | `public/local/edudocuments` |
| `usercontract.zip` | `mod_usercontract` | `mod/usercontract` | `public/mod/usercontract` |
| `userstatement.zip` | `mod_userstatement` | `mod/userstatement` | `public/mod/userstatement` |

Сборки отличаются только `version.php` и CSS-классами: Moodle 4.5 использует Bootstrap 4, Moodle 5.x — Bootstrap 5.

## Установка

Администрирование → Плагины → Установить плагин → загрузить ZIP из папки нужной версии. Порядок: `edudocuments.zip`, затем `usercontract.zip` и `userstatement.zip`.

Вручную: распаковать архивы в каталоги из таблицы и выполнить `php admin/cli/upgrade.php`.

## Обновление с Moodle 3.8

Ядро обновляется поэтапно:

- до 4.5: 3.8 → 3.11 → 4.1 → 4.5;
- до 5.3: 3.8 → 3.11 → 4.1 → 4.5 → 5.3 (5.3 обновляется только с 4.4 и выше).

На промежуточных шагах папки этих плагинов можно убрать из кода — их таблицы и данные остаются в БД.
На целевой версии установите архивы из соответствующей папки: Moodle обновит плагины и сохранит договоры и заявления.
При переходе с 4.5 на 5.3 установите поверх архивы из `moodle-5.3/` — номер их версии выше, Moodle выполнит обычное обновление.
