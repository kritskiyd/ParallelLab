# Product Backlog

Источник требований: актуальные разделы POA, планирования и прототипирования существующего отчёта, а также карта историй с десятью действиями. Разработка заново не планировалась: сохранены границы P0/MVP, P1/Version 1 и P2/Version 2.

[Таблица GitHub Project](https://github.com/users/kritskiyd/projects/1/views/3) · [Все Issues](https://github.com/kritskiyd/ParallelLab/issues)

## Реестр

Созданы 10 Epic, 53 PBI и 10 технических Task. Все 73 элемента являются реальными открытыми Issues; нативная иерархия содержит 63 родительско-дочерние связи. Draft items не используются.

31 PBI относится к MVP, 12 к Version 1 и 10 к Version 2. Оценка дана только PBI; итоговые суммы не включают родителей и Task повторно. Метка релиза Epic обозначает начало поставки направления, а не его полное завершение.

## Epic

| Issue | Направление | Дочерних PBI |
| --- | --- | --- |
| [E01 / #1](https://github.com/kritskiyd/ParallelLab/issues/1) | Управление вычислительными экспериментами | 5 |
| [E02 / #2](https://github.com/kritskiyd/ParallelLab/issues/2) | Работа с исходным кодом | 5 |
| [E03 / #3](https://github.com/kritskiyd/ParallelLab/issues/3) | Выбор технологии вычислений | 6 |
| [E04 / #4](https://github.com/kritskiyd/ParallelLab/issues/4) | Настройка параметров | 5 |
| [E05 / #5](https://github.com/kritskiyd/ParallelLab/issues/5) | Проверка программного окружения | 4 |
| [E06 / #6](https://github.com/kritskiyd/ParallelLab/issues/6) | Компиляция и запуск экспериментов | 6 |
| [E07 / #7](https://github.com/kritskiyd/ParallelLab/issues/7) | Серийные запуски | 5 |
| [E08 / #8](https://github.com/kritskiyd/ParallelLab/issues/8) | Сохранение и просмотр результатов | 6 |
| [E09 / #9](https://github.com/kritskiyd/ParallelLab/issues/9) | Анализ производительности | 7 |
| [E10 / #10](https://github.com/kritskiyd/ParallelLab/issues/10) | Характеристики вычислительной системы | 4 |

## MVP

31 PBI; суммарно 126 предварительных SP.

| Issue | Функция | Epic | Приоритет | SP | Спринт | Зависимости |
| --- | --- | --- | --- | --- | --- | --- |
| [M01 / #11](https://github.com/kritskiyd/ParallelLab/issues/11) | Создать вычислительный эксперимент | [E01 / #1](https://github.com/kritskiyd/ParallelLab/issues/1) | P0 | 5 | Sprint 1 | Нет |
| [M02 / #12](https://github.com/kritskiyd/ParallelLab/issues/12) | Открыть сохранённый эксперимент | [E01 / #1](https://github.com/kritskiyd/ParallelLab/issues/1) | P0 | 3 | Sprint 1 | [M01 / #11](https://github.com/kritskiyd/ParallelLab/issues/11) |
| [M03 / #13](https://github.com/kritskiyd/ParallelLab/issues/13) | Перейти в рабочую область текущего эксперимента | [E01 / #1](https://github.com/kritskiyd/ParallelLab/issues/1) | P0 | 5 | Sprint 1 | [M01 / #11](https://github.com/kritskiyd/ParallelLab/issues/11), [M02 / #12](https://github.com/kritskiyd/ParallelLab/issues/12) |
| [M04 / #14](https://github.com/kritskiyd/ParallelLab/issues/14) | Просматривать и редактировать исходный код | [E02 / #2](https://github.com/kritskiyd/ParallelLab/issues/2) | P0 | 5 | Sprint 2 | [M03 / #13](https://github.com/kritskiyd/ParallelLab/issues/13) |
| [M05 / #15](https://github.com/kritskiyd/ParallelLab/issues/15) | Работать с несколькими реализациями одной задачи | [E02 / #2](https://github.com/kritskiyd/ParallelLab/issues/2) | P0 | 5 | Sprint 2 | [M04 / #14](https://github.com/kritskiyd/ParallelLab/issues/14) |
| [M06 / #16](https://github.com/kritskiyd/ParallelLab/issues/16) | Просматривать C++17 после CUDA-трансляции | [E02 / #2](https://github.com/kritskiyd/ParallelLab/issues/2) | P0 | 3 | Sprint 5 | [M09 / #19](https://github.com/kritskiyd/ParallelLab/issues/19) |
| [M07 / #17](https://github.com/kritskiyd/ParallelLab/issues/17) | Выбрать Sequential C++ как базовую реализацию | [E03 / #3](https://github.com/kritskiyd/ParallelLab/issues/3) | P0 | 3 | Sprint 2 | [M05 / #15](https://github.com/kritskiyd/ParallelLab/issues/15) |
| [M08 / #18](https://github.com/kritskiyd/ParallelLab/issues/18) | Выбрать и выполнить OpenMP-реализацию | [E03 / #3](https://github.com/kritskiyd/ParallelLab/issues/3) | P0 | 3 | Sprint 4 | [M07 / #17](https://github.com/kritskiyd/ParallelLab/issues/17), [M12 / #22](https://github.com/kritskiyd/ParallelLab/issues/22), [M14 / #24](https://github.com/kritskiyd/ParallelLab/issues/24), [M18 / #28](https://github.com/kritskiyd/ParallelLab/issues/28) |
| [M09 / #19](https://github.com/kritskiyd/ParallelLab/issues/19) | Выбрать CUDA-транслятор для CPU | [E03 / #3](https://github.com/kritskiyd/ParallelLab/issues/3) | P0 | 8 | Sprint 5 | [M05 / #15](https://github.com/kritskiyd/ParallelLab/issues/15), [M14 / #24](https://github.com/kritskiyd/ParallelLab/issues/24), [M18 / #28](https://github.com/kritskiyd/ParallelLab/issues/28) |
| [M10 / #20](https://github.com/kritskiyd/ParallelLab/issues/20) | Выбрать и выполнить MPI-реализацию | [E03 / #3](https://github.com/kritskiyd/ParallelLab/issues/3) | P0 | 5 | Sprint 4 | [M07 / #17](https://github.com/kritskiyd/ParallelLab/issues/17), [M12 / #22](https://github.com/kritskiyd/ParallelLab/issues/22), [M14 / #24](https://github.com/kritskiyd/ParallelLab/issues/24), [M18 / #28](https://github.com/kritskiyd/ParallelLab/issues/28) |
| [M11 / #21](https://github.com/kritskiyd/ParallelLab/issues/21) | Настроить размер задачи и число повторов | [E04 / #4](https://github.com/kritskiyd/ParallelLab/issues/4) | P0 | 3 | Sprint 3 | [M07 / #17](https://github.com/kritskiyd/ParallelLab/issues/17) |
| [M12 / #22](https://github.com/kritskiyd/ParallelLab/issues/22) | Настроить потоки OpenMP и процессы MPI | [E04 / #4](https://github.com/kritskiyd/ParallelLab/issues/4) | P0 | 3 | Sprint 4 | [M11 / #21](https://github.com/kritskiyd/ParallelLab/issues/21) |
| [M13 / #23](https://github.com/kritskiyd/ParallelLab/issues/23) | Настроить CUDA Grid и Block | [E04 / #4](https://github.com/kritskiyd/ParallelLab/issues/4) | P0 | 3 | Sprint 5 | [M09 / #19](https://github.com/kritskiyd/ParallelLab/issues/19), [M11 / #21](https://github.com/kritskiyd/ParallelLab/issues/21) |
| [M14 / #24](https://github.com/kritskiyd/ParallelLab/issues/24) | Проверить C++ компилятор, OpenMP и MPI Runtime | [E05 / #5](https://github.com/kritskiyd/ParallelLab/issues/5) | P0 | 5 | Sprint 3 | [M07 / #17](https://github.com/kritskiyd/ParallelLab/issues/17) |
| [M15 / #25](https://github.com/kritskiyd/ParallelLab/issues/25) | Диагностировать CUDA-транслятор и ошибки окружения | [E05 / #5](https://github.com/kritskiyd/ParallelLab/issues/5) | P0 | 3 | Sprint 5 | [M09 / #19](https://github.com/kritskiyd/ParallelLab/issues/19), [M14 / #24](https://github.com/kritskiyd/ParallelLab/issues/24) |
| [M16 / #26](https://github.com/kritskiyd/ParallelLab/issues/26) | Скомпилировать выбранную реализацию | [E06 / #6](https://github.com/kritskiyd/ParallelLab/issues/6) | P0 | 5 | Sprint 3 | [M04 / #14](https://github.com/kritskiyd/ParallelLab/issues/14), [M07 / #17](https://github.com/kritskiyd/ParallelLab/issues/17), [M14 / #24](https://github.com/kritskiyd/ParallelLab/issues/24) |
| [M17 / #27](https://github.com/kritskiyd/ParallelLab/issues/27) | Просматривать консоль и сообщения об ошибках | [E06 / #6](https://github.com/kritskiyd/ParallelLab/issues/6) | P0 | 3 | Sprint 4 | [M16 / #26](https://github.com/kritskiyd/ParallelLab/issues/26) |
| [M18 / #28](https://github.com/kritskiyd/ParallelLab/issues/28) | Запустить и остановить вычислительную программу | [E06 / #6](https://github.com/kritskiyd/ParallelLab/issues/6) | P0 | 5 | Sprint 4 | [M11 / #21](https://github.com/kritskiyd/ParallelLab/issues/21), [M16 / #26](https://github.com/kritskiyd/ParallelLab/issues/26), [M17 / #27](https://github.com/kritskiyd/ParallelLab/issues/27) |
| [M19 / #29](https://github.com/kritskiyd/ParallelLab/issues/29) | Выполнить преобразованный CUDA-код на CPU | [E06 / #6](https://github.com/kritskiyd/ParallelLab/issues/6) | P0 | 5 | Sprint 5 | [M06 / #16](https://github.com/kritskiyd/ParallelLab/issues/16), [M13 / #23](https://github.com/kritskiyd/ParallelLab/issues/23), [M15 / #25](https://github.com/kritskiyd/ParallelLab/issues/25), [M18 / #28](https://github.com/kritskiyd/ParallelLab/issues/28) |
| [M20 / #30](https://github.com/kritskiyd/ParallelLab/issues/30) | Создать серию запусков и отслеживать прогресс | [E07 / #7](https://github.com/kritskiyd/ParallelLab/issues/7) | P0 | 5 | Sprint 6 | [M08 / #18](https://github.com/kritskiyd/ParallelLab/issues/18), [M10 / #20](https://github.com/kritskiyd/ParallelLab/issues/20), [M19 / #29](https://github.com/kritskiyd/ParallelLab/issues/29) |
| [M21 / #31](https://github.com/kritskiyd/ParallelLab/issues/31) | Перебирать потоки, процессы и размер задачи | [E07 / #7](https://github.com/kritskiyd/ParallelLab/issues/7) | P0 | 5 | Sprint 6 | [M20 / #30](https://github.com/kritskiyd/ParallelLab/issues/30) |
| [M22 / #32](https://github.com/kritskiyd/ParallelLab/issues/32) | Выполнить повторы каждой конфигурации | [E07 / #7](https://github.com/kritskiyd/ParallelLab/issues/7) | P0 | 3 | Sprint 6 | [M20 / #30](https://github.com/kritskiyd/ParallelLab/issues/30), [M21 / #31](https://github.com/kritskiyd/ParallelLab/issues/31) |
| [M23 / #33](https://github.com/kritskiyd/ParallelLab/issues/33) | Просматривать базовую историю запусков | [E08 / #8](https://github.com/kritskiyd/ParallelLab/issues/8) | P0 | 5 | Sprint 7 | [M18 / #28](https://github.com/kritskiyd/ParallelLab/issues/28), [M20 / #30](https://github.com/kritskiyd/ParallelLab/issues/30), [M25 / #35](https://github.com/kritskiyd/ParallelLab/issues/35) |
| [M24 / #34](https://github.com/kritskiyd/ParallelLab/issues/34) | Просматривать детали и таблицу результатов запуска | [E08 / #8](https://github.com/kritskiyd/ParallelLab/issues/8) | P0 | 3 | Sprint 7 | [M25 / #35](https://github.com/kritskiyd/ParallelLab/issues/35) |
| [M25 / #35](https://github.com/kritskiyd/ParallelLab/issues/35) | Сохранить результат с условиями эксперимента | [E08 / #8](https://github.com/kritskiyd/ParallelLab/issues/8) | P0 | 3 | Sprint 7 | [M18 / #28](https://github.com/kritskiyd/ParallelLab/issues/28), [M31 / #41](https://github.com/kritskiyd/ParallelLab/issues/41) |
| [M26 / #36](https://github.com/kritskiyd/ParallelLab/issues/36) | Сравнить время выполнения реализаций | [E09 / #9](https://github.com/kritskiyd/ParallelLab/issues/9) | P0 | 5 | Sprint 8 | [M24 / #34](https://github.com/kritskiyd/ParallelLab/issues/34), [M08 / #18](https://github.com/kritskiyd/ParallelLab/issues/18), [M10 / #20](https://github.com/kritskiyd/ParallelLab/issues/20), [M19 / #29](https://github.com/kritskiyd/ParallelLab/issues/29) |
| [M27 / #37](https://github.com/kritskiyd/ParallelLab/issues/37) | Рассчитать ускорение относительно Sequential C++ | [E09 / #9](https://github.com/kritskiyd/ParallelLab/issues/9) | P0 | 3 | Sprint 8 | [M26 / #36](https://github.com/kritskiyd/ParallelLab/issues/36) |
| [M28 / #38](https://github.com/kritskiyd/ParallelLab/issues/38) | Рассчитать эффективность OpenMP и MPI | [E09 / #9](https://github.com/kritskiyd/ParallelLab/issues/9) | P0 | 3 | Sprint 8 | [M27 / #37](https://github.com/kritskiyd/ParallelLab/issues/37), [M12 / #22](https://github.com/kritskiyd/ParallelLab/issues/22) |
| [M29 / #39](https://github.com/kritskiyd/ParallelLab/issues/39) | Построить базовый график и выбрать оси | [E09 / #9](https://github.com/kritskiyd/ParallelLab/issues/9) | P0 | 5 | Sprint 8 | [M26 / #36](https://github.com/kritskiyd/ParallelLab/issues/36), [M27 / #37](https://github.com/kritskiyd/ParallelLab/issues/37), [M28 / #38](https://github.com/kritskiyd/ParallelLab/issues/38) |
| [M30 / #40](https://github.com/kritskiyd/ParallelLab/issues/40) | Просмотреть CPU, RAM, GPU и ОС | [E10 / #10](https://github.com/kritskiyd/ParallelLab/issues/10) | P0 | 3 | Sprint 7 | [M14 / #24](https://github.com/kritskiyd/ParallelLab/issues/24) |
| [M31 / #41](https://github.com/kritskiyd/ParallelLab/issues/41) | Связать снимок системы с результатом запуска | [E10 / #10](https://github.com/kritskiyd/ParallelLab/issues/10) | P0 | 3 | Sprint 7 | [M30 / #40](https://github.com/kritskiyd/ParallelLab/issues/40), [M18 / #28](https://github.com/kritskiyd/ParallelLab/issues/28) |

## Version 1

12 PBI; суммарно 53 предварительных SP.

| Issue | Функция | Epic | Приоритет | SP | Спринт | Зависимости |
| --- | --- | --- | --- | --- | --- | --- |
| [V101 / #42](https://github.com/kritskiyd/ParallelLab/issues/42) | Создать эксперимент из шаблона | [E01 / #1](https://github.com/kritskiyd/ParallelLab/issues/1) | P1 | 5 | Не назначен | [M01 / #11](https://github.com/kritskiyd/ParallelLab/issues/11), [M05 / #15](https://github.com/kritskiyd/ParallelLab/issues/15) |
| [V102 / #43](https://github.com/kritskiyd/ParallelLab/issues/43) | Просмотреть историю изменений исходного кода | [E02 / #2](https://github.com/kritskiyd/ParallelLab/issues/2) | P1 | 5 | Не назначен | [M04 / #14](https://github.com/kritskiyd/ParallelLab/issues/14), [M25 / #35](https://github.com/kritskiyd/ParallelLab/issues/35) |
| [V103 / #44](https://github.com/kritskiyd/ParallelLab/issues/44) | Выбрать CUDA Native или CUDA-транслятор | [E03 / #3](https://github.com/kritskiyd/ParallelLab/issues/3) | P1 | 3 | Не назначен | [M09 / #19](https://github.com/kritskiyd/ParallelLab/issues/19), [V105 / #46](https://github.com/kritskiyd/ParallelLab/issues/46) |
| [V104 / #45](https://github.com/kritskiyd/ParallelLab/issues/45) | Сохранить и применить набор параметров | [E04 / #4](https://github.com/kritskiyd/ParallelLab/issues/4) | P1 | 3 | Не назначен | [M11 / #21](https://github.com/kritskiyd/ParallelLab/issues/21), [M12 / #22](https://github.com/kritskiyd/ParallelLab/issues/22), [M13 / #23](https://github.com/kritskiyd/ParallelLab/issues/23) |
| [V105 / #46](https://github.com/kritskiyd/ParallelLab/issues/46) | Проверить CUDA Toolkit и NVIDIA GPU | [E05 / #5](https://github.com/kritskiyd/ParallelLab/issues/5) | P1 | 5 | Не назначен | [M14 / #24](https://github.com/kritskiyd/ParallelLab/issues/24), [M15 / #25](https://github.com/kritskiyd/ParallelLab/issues/25) |
| [V106 / #47](https://github.com/kritskiyd/ParallelLab/issues/47) | Собрать и выполнить CUDA Native на GPU | [E06 / #6](https://github.com/kritskiyd/ParallelLab/issues/6) | P1 | 8 | Не назначен | [V103 / #44](https://github.com/kritskiyd/ParallelLab/issues/44), [V105 / #46](https://github.com/kritskiyd/ParallelLab/issues/46), [M18 / #28](https://github.com/kritskiyd/ParallelLab/issues/28), [M25 / #35](https://github.com/kritskiyd/ParallelLab/issues/35) |
| [V107 / #48](https://github.com/kritskiyd/ParallelLab/issues/48) | Применить сохранённый план серии | [E07 / #7](https://github.com/kritskiyd/ParallelLab/issues/7) | P1 | 3 | Не назначен | [M20 / #30](https://github.com/kritskiyd/ParallelLab/issues/30), [M21 / #31](https://github.com/kritskiyd/ParallelLab/issues/31), [M22 / #32](https://github.com/kritskiyd/ParallelLab/issues/32), [V104 / #45](https://github.com/kritskiyd/ParallelLab/issues/45) |
| [V108 / #49](https://github.com/kritskiyd/ParallelLab/issues/49) | Искать и фильтровать историю запусков | [E08 / #8](https://github.com/kritskiyd/ParallelLab/issues/8) | P1 | 3 | Не назначен | [M23 / #33](https://github.com/kritskiyd/ParallelLab/issues/33) |
| [V109 / #50](https://github.com/kritskiyd/ParallelLab/issues/50) | Экспортировать таблицу и графики результатов | [E08 / #8](https://github.com/kritskiyd/ParallelLab/issues/8) | P1 | 5 | Не назначен | [M24 / #34](https://github.com/kritskiyd/ParallelLab/issues/34), [M29 / #39](https://github.com/kritskiyd/ParallelLab/issues/39) |
| [V110 / #51](https://github.com/kritskiyd/ParallelLab/issues/51) | Использовать дополнительные графики анализа | [E09 / #9](https://github.com/kritskiyd/ParallelLab/issues/9) | P1 | 5 | Не назначен | [M29 / #39](https://github.com/kritskiyd/ParallelLab/issues/39) |
| [V111 / #52](https://github.com/kritskiyd/ParallelLab/issues/52) | Сопоставить CUDA Native и CUDA-транслятор | [E09 / #9](https://github.com/kritskiyd/ParallelLab/issues/9) | P1 | 5 | Не назначен | [V106 / #47](https://github.com/kritskiyd/ParallelLab/issues/47), [M19 / #29](https://github.com/kritskiyd/ParallelLab/issues/29), [M26 / #36](https://github.com/kritskiyd/ParallelLab/issues/36) |
| [V112 / #53](https://github.com/kritskiyd/ParallelLab/issues/53) | Сформировать отчёт о конфигурации системы | [E10 / #10](https://github.com/kritskiyd/ParallelLab/issues/10) | P1 | 3 | Не назначен | [M31 / #41](https://github.com/kritskiyd/ParallelLab/issues/41) |

## Version 2

10 PBI; суммарно 65 предварительных SP.

| Issue | Функция | Epic | Приоритет | SP | Спринт | Зависимости |
| --- | --- | --- | --- | --- | --- | --- |
| [V201 / #54](https://github.com/kritskiyd/ParallelLab/issues/54) | Вести архив экспериментов | [E01 / #1](https://github.com/kritskiyd/ParallelLab/issues/1) | P2 | 3 | Не назначен | [M02 / #12](https://github.com/kritskiyd/ParallelLab/issues/12), [M25 / #35](https://github.com/kritskiyd/ParallelLab/issues/35) |
| [V202 / #55](https://github.com/kritskiyd/ParallelLab/issues/55) | Совместно работать и обсуждать код эксперимента | [E02 / #2](https://github.com/kritskiyd/ParallelLab/issues/2) | P2 | 8 | Не назначен | [V102 / #43](https://github.com/kritskiyd/ParallelLab/issues/43) |
| [V203 / #56](https://github.com/kritskiyd/ParallelLab/issues/56) | Выбрать профиль вычислительного ресурса | [E03 / #3](https://github.com/kritskiyd/ParallelLab/issues/3) | P2 | 5 | Не назначен | [M07 / #17](https://github.com/kritskiyd/ParallelLab/issues/17), [V103 / #44](https://github.com/kritskiyd/ParallelLab/issues/44) |
| [V204 / #57](https://github.com/kritskiyd/ParallelLab/issues/57) | Использовать общие конфигурации параметров | [E04 / #4](https://github.com/kritskiyd/ParallelLab/issues/4) | P2 | 5 | Не назначен | [V104 / #45](https://github.com/kritskiyd/ParallelLab/issues/45), [V202 / #55](https://github.com/kritskiyd/ParallelLab/issues/55) |
| [V205 / #58](https://github.com/kritskiyd/ParallelLab/issues/58) | Проверить доступность удалённого узла | [E05 / #5](https://github.com/kritskiyd/ParallelLab/issues/5) | P2 | 5 | Не назначен | [V203 / #56](https://github.com/kritskiyd/ParallelLab/issues/56), [M14 / #24](https://github.com/kritskiyd/ParallelLab/issues/24) |
| [V206 / #59](https://github.com/kritskiyd/ParallelLab/issues/59) | Выполнить эксперимент на удалённом ресурсе | [E06 / #6](https://github.com/kritskiyd/ParallelLab/issues/6) | P2 | 13 | Не назначен | [V205 / #58](https://github.com/kritskiyd/ParallelLab/issues/58), [M18 / #28](https://github.com/kritskiyd/ParallelLab/issues/28), [M25 / #35](https://github.com/kritskiyd/ParallelLab/issues/35) |
| [V207 / #60](https://github.com/kritskiyd/ParallelLab/issues/60) | Выполнить распределённую серию запусков | [E07 / #7](https://github.com/kritskiyd/ParallelLab/issues/7) | P2 | 8 | Не назначен | [V206 / #59](https://github.com/kritskiyd/ParallelLab/issues/59), [M20 / #30](https://github.com/kritskiyd/ParallelLab/issues/30), [M22 / #32](https://github.com/kritskiyd/ParallelLab/issues/32) |
| [V208 / #61](https://github.com/kritskiyd/ParallelLab/issues/61) | Передать результаты исследования участникам | [E08 / #8](https://github.com/kritskiyd/ParallelLab/issues/8) | P2 | 5 | Не назначен | [V202 / #55](https://github.com/kritskiyd/ParallelLab/issues/55), [V109 / #50](https://github.com/kritskiyd/ParallelLab/issues/50) |
| [V209 / #62](https://github.com/kritskiyd/ParallelLab/issues/62) | Исследовать устойчивость измерений | [E09 / #9](https://github.com/kritskiyd/ParallelLab/issues/9) | P2 | 8 | Не назначен | [M22 / #32](https://github.com/kritskiyd/ParallelLab/issues/32), [V110 / #51](https://github.com/kritskiyd/ParallelLab/issues/51) |
| [V210 / #63](https://github.com/kritskiyd/ParallelLab/issues/63) | Сопоставить результаты разных вычислительных систем | [E10 / #10](https://github.com/kritskiyd/ParallelLab/issues/10) | P2 | 5 | Не назначен | [M31 / #41](https://github.com/kritskiyd/ParallelLab/issues/41), [V112 / #53](https://github.com/kritskiyd/ParallelLab/issues/53), [V209 / #62](https://github.com/kritskiyd/ParallelLab/issues/62) |

## Task первого спринта

| Issue | Технический результат | Родительский PBI |
| --- | --- | --- |
| [T01 / #64](https://github.com/kritskiyd/ParallelLab/issues/64) | Описать локальный формат эксперимента и правила валидации | [M01 / #11](https://github.com/kritskiyd/ParallelLab/issues/11) |
| [T02 / #65](https://github.com/kritskiyd/ParallelLab/issues/65) | Реализовать форму создания эксперимента | [M01 / #11](https://github.com/kritskiyd/ParallelLab/issues/11) |
| [T03 / #66](https://github.com/kritskiyd/ParallelLab/issues/66) | Реализовать безопасную запись нового эксперимента | [M01 / #11](https://github.com/kritskiyd/ParallelLab/issues/11) |
| [T04 / #67](https://github.com/kritskiyd/ParallelLab/issues/67) | Проверить создание эксперимента и обработку ошибок | [M01 / #11](https://github.com/kritskiyd/ParallelLab/issues/11) |
| [T05 / #68](https://github.com/kritskiyd/ParallelLab/issues/68) | Реализовать загрузку и проверку формата эксперимента | [M02 / #12](https://github.com/kritskiyd/ParallelLab/issues/12) |
| [T06 / #69](https://github.com/kritskiyd/ParallelLab/issues/69) | Реализовать выбор файла и ошибки открытия | [M02 / #12](https://github.com/kritskiyd/ParallelLab/issues/12) |
| [T07 / #70](https://github.com/kritskiyd/ParallelLab/issues/70) | Проверить повторное открытие сохранённого эксперимента | [M02 / #12](https://github.com/kritskiyd/ParallelLab/issues/12) |
| [T08 / #71](https://github.com/kritskiyd/ParallelLab/issues/71) | Собрать рабочую область на основе существующего прототипа | [M03 / #13](https://github.com/kritskiyd/ParallelLab/issues/13) |
| [T09 / #72](https://github.com/kritskiyd/ParallelLab/issues/72) | Реализовать единый контекст текущего эксперимента | [M03 / #13](https://github.com/kritskiyd/ParallelLab/issues/13) |
| [T10 / #73](https://github.com/kritskiyd/ParallelLab/issues/73) | Проверить навигацию и состояния рабочей области | [M03 / #13](https://github.com/kritskiyd/ParallelLab/issues/13) |

## Приоритеты и актуализация

P0 проверяет полный локальный пользовательский сценарий, P1 расширяет его Native GPU-режимом и удобством повторной работы, P2 поддерживает совместные и удалённые исследования. Роли в историях взяты из POA: студент, преподаватель, специалист атомной отрасли.

Оценки предварительны и не являются обещанием сроков. Изменения согласуются на Planning и отражаются в Issue, milestone, метках и полях проекта. Состояние фактической настройки полей приведено в [конфигурации](Project-Configuration.md).

[К плану спринтов](Sprint-Planning.md) · [К навигации](Home.md)
