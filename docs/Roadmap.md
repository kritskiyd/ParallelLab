# План выпусков

## Первый выпуск (MVP)

31 история, 126 условных единиц, 13 планируемых спринтов. Полный локальный сценарий: создание или открытие эксперимента, редактор и несколько реализаций, Sequential C++, OpenMP, MPI, CUDA-транслятор / CPU, параметры, окружение, компиляция, консоль, запуск и остановка, серия, сохранение и базовая история, таблицы, сравнение и график, снимок системы.

Первый выпуск готов, когда выполнены критерии историй, вычисления проверены на тестовых данных и пройден полный пользовательский сценарий, включая обработку ошибок и сохранение результатов.

## Второй выпуск

- [Создать эксперимент из шаблона](https://github.com/kritskiyd/ParallelLab/issues/42)
- [Просмотреть историю изменений исходного кода](https://github.com/kritskiyd/ParallelLab/issues/43)
- [Выбрать CUDA Native или CUDA-транслятор](https://github.com/kritskiyd/ParallelLab/issues/44)
- [Сохранить и применить набор параметров](https://github.com/kritskiyd/ParallelLab/issues/45)
- [Проверить CUDA Toolkit и NVIDIA GPU](https://github.com/kritskiyd/ParallelLab/issues/46)
- [Собрать и выполнить CUDA Native на GPU](https://github.com/kritskiyd/ParallelLab/issues/47)
- [Применить сохранённый план серии](https://github.com/kritskiyd/ParallelLab/issues/48)
- [Искать и фильтровать историю запусков](https://github.com/kritskiyd/ParallelLab/issues/49)
- [Экспортировать таблицу и графики результатов](https://github.com/kritskiyd/ParallelLab/issues/50)
- [Использовать дополнительные графики анализа](https://github.com/kritskiyd/ParallelLab/issues/51)
- [Сопоставить CUDA Native и CUDA-транслятор](https://github.com/kritskiyd/ParallelLab/issues/52)
- [Сформировать отчёт о конфигурации системы](https://github.com/kritskiyd/ParallelLab/issues/53)

## Третий выпуск

- [Вести архив экспериментов](https://github.com/kritskiyd/ParallelLab/issues/54)
- [Совместно работать и обсуждать код эксперимента](https://github.com/kritskiyd/ParallelLab/issues/55)
- [Выбрать профиль вычислительного ресурса](https://github.com/kritskiyd/ParallelLab/issues/56)
- [Использовать общие конфигурации параметров](https://github.com/kritskiyd/ParallelLab/issues/57)
- [Проверить доступность удалённого узла](https://github.com/kritskiyd/ParallelLab/issues/58)
- [Выполнить эксперимент на удалённом ресурсе](https://github.com/kritskiyd/ParallelLab/issues/59)
- [Выполнить распределённую серию запусков](https://github.com/kritskiyd/ParallelLab/issues/60)
- [Передать результаты исследования участникам](https://github.com/kritskiyd/ParallelLab/issues/61)
- [Исследовать устойчивость измерений](https://github.com/kritskiyd/ParallelLab/issues/62)
- [Сопоставить результаты разных вычислительных систем](https://github.com/kritskiyd/ParallelLab/issues/63)

Сроки реализации следующих 22 историй будут определены после первого выпуска. При планировании их оценки могут быть уточнены. Для CUDA Native нужны совместимая NVIDIA GPU и CUDA Toolkit; CPU-режим транслятора от них не зависит.

[Бэклог](Product-Backlog.md) · [Спринты](Sprint-Planning.md) · [Навигация](Home.md)
