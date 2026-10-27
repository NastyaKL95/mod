# Плагины Moodle 5.3

| Архив | Компонент | Куда устанавливается |
| --- | --- | --- |
| `edudocuments.zip` | `local_edudocuments` | `public/local/edudocuments` |
| `usercontract.zip` | `mod_usercontract` | `public/mod/usercontract` |
| `userstatement.zip` | `mod_userstatement` | `public/mod/userstatement` |

Требуется Moodle 5.3 (`requires = 2026100500`).

## Установка

Администрирование → Плагины → Установить плагин → загрузить ZIP. Порядок: `edudocuments.zip`, затем `usercontract.zip` и `userstatement.zip`.

Вручную: распаковать архивы в `public/local/` и `public/mod/` и выполнить `php admin/cli/upgrade.php`.

## Обновление с Moodle 3.8

Moodle 5.3 обновляется только с 4.4 и выше, поэтому ядро обновляется поэтапно: 3.8 → 3.11 → 4.4 → 5.3.
На промежуточных шагах папки этих плагинов можно убрать из кода — их таблицы и данные остаются в БД.
После перехода на 5.3 установите архивы: Moodle выполнит обновление плагинов и сохранит договоры и заявления.
