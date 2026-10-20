# Конфигурация GitHub Project

## Существующие объекты

Владелец: `kritskiyd`. Проект № 1: [ParallelLab Scrum Development](https://github.com/users/kritskiyd/projects/1). Репозиторий: [kritskiyd/ParallelLab](https://github.com/kritskiyd/ParallelLab). Оба объекта приватные; видимость не менялась. Default repository проекта указывает на этот репозиторий.

Шаблон Iterative development сохранён. Переиспользованы представления Current Sprint (бывшее Current iteration), Next Sprint (бывшее Next iteration), Product Backlog (бывшее Prioritized backlog) и Roadmap. Представления In review и My items оставлены без дублирования.

## Поля

Status: Backlog, Ready, In Progress, In Review, Done. Priority: P0, P1, P2. Существующее числовое Estimate переименовано в Story Points. Добавлено поле Release: MVP, Version 1, Version 2. Существующее Iteration содержит восемь двухнедельных спринтов. Size не удалено, но скрыто из основного бэклога.

Product Backlog использует таблицу, содержит Title, Assignees, Status, Priority, Story Points, Iteration, Release и Parent issue; сортировка по Priority по возрастанию. Связи Parent issue дополняются нативными Sub-issues. Все элементы являются Issues, а не draft items.

## Автоматизации

Подтверждено автоматическое добавление новых открытых Issues из ParallelLab и назначение им Backlog. Это видно в timeline реальных созданных историй. Включён workflow добавления дочерних Issues. Остальные workflows проверяются через интерфейс перед итоговым обновлением этого документа.

Завершение и архивирование не проверяются закрытием фиктивных задач. Ни одна функция продукта не объявлена реализованной. Автоархивирование для нового бэклога не требуется.

## Ограничение доступа

Действующий вход Git позволяет работать с репозиторием и Issues, но GraphQL Projects возвращает INSUFFICIENT_SCOPES: отсутствует read:project/project. Права входа не расширялись. Поля и представления настраиваются через разрешённый браузерный интерфейс. Это ограничение API не означает, что репозиторий или Project являются публичными.

Точное состояние заполнения нативных полей и итоговой проверки должно быть зафиксировано после её завершения; наличие значений в тексте Issue само по себе не считается заполнением поля Project.

[К процессу](Scrum-Process.md) · [К навигации](Home.md)
