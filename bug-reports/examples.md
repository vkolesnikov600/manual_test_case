# Bug Report 

## BUG-001 - Некорректная работа нескольких фильтров одновременно.

| Field | Value |
| --- | --- |
| Severity | Major |
| Priority | High |
| Environment | Web, Chrome, Windows 11 |
| Build | 1.0.0 |
| Status | Open |

## Preconditions
Находиться в каталоге. 


## Steps To Reproduce

1. Открыть каталог.
2. Выбрать бренд Samsung.
3. Выбрать бренд Xiaomi.
4. Нажать "Применить".

## Actual Result

Отображаются товары только Samsung.

## Expected Result

Отображаются товары Samsung и Xiaomi.


## BUG-002 - Кнопка "Сбросить фильтры" не очищает диапазон цены.

| Field | Value |
| --- | --- |
| Severity | Minor |
| Priority | Medium |
| Environment | Android 14, Pixel 7 |
| Build | 2.4.1 |
| Status | Open |

## Preconditions

Находиться на странице фильтров.

## Steps To Reproduce

Шаги:
Установить цену от 5000 до 10000.
Нажать "Применить".
Нажать "Сбросить фильтры".
## Actual Result

Диапазон цены остается заполненным.

## Expected Result

Все фильтры должны быть очищены.

