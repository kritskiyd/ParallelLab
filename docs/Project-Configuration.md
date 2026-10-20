# Конфигурация GitHub Project

## Существующие объекты

Владелец: `kritskiyd`. Проект № 1: [ParallelLab Scrum Development](https://github.com/users/kritskiyd/projects/1). Репозиторий: [kritskiyd/ParallelLab](https://github.com/kritskiyd/ParallelLab). Оба объекта приватные; видимость не менялась. Default repository проекта указывает на этот репозиторий. На вкладке Projects репозитория подтверждён один связанный приватный проект с этим названием и номером.

Шаблон Iterative development сохранён. Переиспользованы представления Current Sprint (бывшее Current iteration), Next Sprint (бывшее Next iteration), Product Backlog (бывшее Prioritized backlog) и Roadmap. Представления In review и My items оставлены без дублирования.

## Поля

Status: Backlog, Ready, In Progress, In Review, Done. Priority: P0, P1, P2. Существующее числовое Estimate переименовано в Story Points. Добавлено поле Release: MVP, Version 1, Version 2. Существующее Iteration содержит восемь двухнедельных спринтов. Size не удалено, но скрыто из основного бэклога.

Product Backlog использует таблицу, содержит Title, Assignees, Status, Priority, Story Points, Iteration, Release и Parent issue; сортировка по Priority по возрастанию. Связи Parent issue дополняются нативными Sub-issues. Все элементы являются Issues, а не draft items.

Current Sprint использует доску по Status и фильтр `iteration:@current`: 3 PBI и 10 Task, 13 SP. Next Sprint использует `iteration:@next`: 3 PBI, 13 SP. Из Backlog текущей доски убран лимит размера колонки, который не соответствует накопительной очереди задач. Roadmap сгруппирован по Release, отфильтрован по `label:pbi` и использует Iteration start/end для временных интервалов. Version 1/2 отображаются без выдуманных дат.

Для классификации использованы Labels. Issue Types предназначены для репозиториев организации; в интерфейсе этого личного репозитория поле типа недоступно. Перенос в организацию ради типов не выполнялся. См. [описание Issue Types](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/managing-issue-types-in-an-organization).

## Проверка заполнения

20.10.2026 выполнен штатный экспорт Product Backlog в TSV после повторной загрузки страницы. Все 73 строки сверены с планом: Priority и Release заполнены у всех, Story Points заполнены у 53 PBI, Iteration назначен 31 PBI MVP и 10 Task первого спринта. У 63 дочерних элементов верен Parent issue. Повторная проверка не выявила расхождений. Оценки Epic и Task оставлены пустыми во избежание двойного учёта. Все 73 Issue открыты, статус каждого в Project равен Backlog.

ГрафQL-чтением Issues независимо проверены 63 нативные связи в обоих направлениях. Принадлежность Project подтверждена для 73 из 73 Issues. Assignees оставлены пустыми до фактического принятия работы; вымышленные исполнители не назначались.

## Автоматизации

Включены и проверены восемь встроенных workflows:

| Workflow | Условие и действие |
| --- | --- |
| Auto-add to project | Новая или обновлённая открытая Issue из ParallelLab соответствует `is:issue is:open` и добавляется в Project |
| Auto-add sub-issues to project | Дочерние Issues элемента добавляются в Project |
| Item added to project | Добавленный элемент получает Backlog |
| Item closed | Закрытый элемент получает Done |
| Pull request linked to issue | Связанный с PR Issue получает In Progress, но не Done |
| Pull request merged | Объединённый PR как элемент Project получает Done; это не самостоятельное подтверждение критериев PBI |
| Auto-close issue | Issue закрывается при осознанном переводе его статуса в Done |
| Item reopened | Переоткрытый элемент возвращается в Backlog; правило добавлено при настройке |

Auto-add и Backlog подтверждены timeline реально созданных историй. Правила закрытия и слияния проверены по конфигурации, но не имитировались фиктивными завершёнными задачами. `Closes #N` допустимо только после полного выполнения критериев; для частичной работы используется `Refs #N`. Автоматического завершения всех родительских PBI по одной дочерней Task нет. См. [встроенные автоматизации GitHub](https://docs.github.com/en/issues/planning-and-tracking-with-projects/automating-your-project/using-the-built-in-automations).

Завершение и архивирование не проверяются закрытием фиктивных задач. Ни одна функция продукта не объявлена реализованной. Автоархивирование для нового бэклога не требуется.

## Ограничение доступа

Действующий вход Git позволяет работать с репозиторием и Issues, но GraphQL Projects возвращает INSUFFICIENT_SCOPES: отсутствует read:project/project. Права входа не расширялись. Поля и представления настраиваются через разрешённый браузерный интерфейс. Это ограничение API не означает, что репозиторий или Project являются публичными.

Отсутствие GitHub CLI компенсировано REST API и браузером. Существенных незавершённых операций по настройке нет. Не выполнялись и не требовались расширение прав токена, включение недоступного GitHub Wiki, создание организации, платные изменения тарифа и фиктивное выполнение функциональных задач.

[К процессу](Scrum-Process.md) · [К навигации](Home.md)
