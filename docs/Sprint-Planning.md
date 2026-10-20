# Планирование спринтов

## Основания и допущения

Сохранено существующее поле Iteration и его дата начала 20.10.2026. Пять итераций шаблона переименованы в Sprint 1–5; добавлены Sprint 6–8. Длительность каждой итерации составляет 14 календарных дней. План не содержит произвольно назначенных прошедших дат.

Реальная velocity ещё не измерена. Набор 13–22 SP на спринт является предварительным разбиением по зависимостям, а не подтверждённой производительностью одного разработчика. Sprint 5 имеет повышенную неопределённость из-за границ CUDA-транслятора. На Planning этот объём нужно уточнить, при необходимости перенести целую историю в дополнительную итерацию.

Праздники и доступность разработчика на рубеже года не считаются рабочими днями автоматически. Календарь шаблона сохранён как предварительная сетка; обязательства формируются после согласования доступности.

## План MVP

| Итерация | Даты включительно | Тема | PBI | SP | Sprint Goal |
| --- | --- | --- | --- | --- | --- |
| Sprint 1 | 20.10.2026–02.11.2026 | Основа эксперимента | [M01 / #11](https://github.com/kritskiyd/ParallelLab/issues/11), [M02 / #12](https://github.com/kritskiyd/ParallelLab/issues/12), [M03 / #13](https://github.com/kritskiyd/ParallelLab/issues/13) | 13 | Создать и повторно открыть эксперимент в рабочей области. |
| Sprint 2 | 03.11.2026–16.11.2026 | Исходный код | [M04 / #14](https://github.com/kritskiyd/ParallelLab/issues/14), [M05 / #15](https://github.com/kritskiyd/ParallelLab/issues/15), [M07 / #17](https://github.com/kritskiyd/ParallelLab/issues/17) | 13 | Подготовить несколько реализаций и последовательную базу. |
| Sprint 3 | 17.11.2026–30.11.2026 | Подготовка сборки | [M11 / #21](https://github.com/kritskiyd/ParallelLab/issues/21), [M14 / #24](https://github.com/kritskiyd/ParallelLab/issues/24), [M16 / #26](https://github.com/kritskiyd/ParallelLab/issues/26) | 13 | Проверить CPU-окружение, параметры и собрать программу. |
| Sprint 4 | 01.12.2026–14.12.2026 | Управляемый параллельный запуск | [M08 / #18](https://github.com/kritskiyd/ParallelLab/issues/18), [M10 / #20](https://github.com/kritskiyd/ParallelLab/issues/20), [M12 / #22](https://github.com/kritskiyd/ParallelLab/issues/22), [M17 / #27](https://github.com/kritskiyd/ParallelLab/issues/27), [M18 / #28](https://github.com/kritskiyd/ParallelLab/issues/28) | 19 | Выполнить и остановить Sequential, OpenMP и MPI с понятной консолью. |
| Sprint 5 | 15.12.2026–28.12.2026 | CUDA на CPU | [M06 / #16](https://github.com/kritskiyd/ParallelLab/issues/16), [M09 / #19](https://github.com/kritskiyd/ParallelLab/issues/19), [M13 / #23](https://github.com/kritskiyd/ParallelLab/issues/23), [M15 / #25](https://github.com/kritskiyd/ParallelLab/issues/25), [M19 / #29](https://github.com/kritskiyd/ParallelLab/issues/29) | 22 | Преобразовать поддерживаемый CUDA-код и выполнить его на CPU без NVIDIA GPU. |
| Sprint 6 | 29.12.2026–11.01.2027 | Серийный эксперимент | [M20 / #30](https://github.com/kritskiyd/ParallelLab/issues/30), [M21 / #31](https://github.com/kritskiyd/ParallelLab/issues/31), [M22 / #32](https://github.com/kritskiyd/ParallelLab/issues/32) | 13 | Пройти план перебора параметров с повторами и прогрессом. |
| Sprint 7 | 12.01.2027–25.01.2027 | Сохранённый результат | [M23 / #33](https://github.com/kritskiyd/ParallelLab/issues/33), [M24 / #34](https://github.com/kritskiyd/ParallelLab/issues/34), [M25 / #35](https://github.com/kritskiyd/ParallelLab/issues/35), [M30 / #40](https://github.com/kritskiyd/ParallelLab/issues/40), [M31 / #41](https://github.com/kritskiyd/ParallelLab/issues/41) | 17 | Повторно открыть результат с ревизией и снимком системы. |
| Sprint 8 | 26.01.2027–08.02.2027 | Сравнительный анализ MVP | [M26 / #36](https://github.com/kritskiyd/ParallelLab/issues/36), [M27 / #37](https://github.com/kritskiyd/ParallelLab/issues/37), [M28 / #38](https://github.com/kritskiyd/ParallelLab/issues/38), [M29 / #39](https://github.com/kritskiyd/ParallelLab/issues/39) | 16 | Сопоставить корректные измерения и пройти полный сценарий MVP. |

Итого: 31 PBI, 126 SP. Спринт 7 реализует устойчивое хранение и историю; до него запуски и серии демонстрируют временные результаты в рамках сессии, без обещания готового постоянного журнала.

## Ближайший Sprint Backlog

Выбраны [M01 / #11](https://github.com/kritskiyd/ParallelLab/issues/11), [M02 / #12](https://github.com/kritskiyd/ParallelLab/issues/12), [M03 / #13](https://github.com/kritskiyd/ParallelLab/issues/13): 13 SP и 10 технических Task. Зависимость внутри спринта: сначала формат и создание, затем открытие, затем единый контекст рабочей области.

Task содержат конкретные результаты: формат и валидация, интерфейс и атомарная запись, загрузка и проверка ошибок, IDE-компоновка и навигация. Их критерии доступны через [реестр](Product-Backlog.md).

Планирование не выдаётся за начало разработки. Статус Backlog сохраняется до подтверждения Definition of Ready и реального принятия работы исполнителем.

## Зависимости

До OpenMP/MPI нужны код, базовая сборка, окружение и управление процессом. CUDA-трансляция зависит от CPU-конвейера; Native GPU-режим не является её зависимостью. Серия использует готовые одиночные запуски; сохранение связывает результат со снимком системы. Аналитика использует корректные сохранённые записи. Все прямые зависимости перечислены в PBI; циклов нет.

## Последующие релизы

Version 1 и Version 2 остаются в Product Backlog с предварительными SP, без выдуманных дат или преждевременной технической декомпозиции. Спринты этих релизов выбираются после Review MVP и уточнения скорости разработки.

[Current Sprint](https://github.com/users/kritskiyd/projects/1/views/1) · [Next Sprint](https://github.com/users/kritskiyd/projects/1/views/2) · [Roadmap](Roadmap.md) · [Навигация](Home.md)
