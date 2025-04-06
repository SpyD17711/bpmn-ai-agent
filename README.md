# Система визуализации BPMN-диаграмм

## Описание задачи 
**Цель:** разработать сервис, который поможет аналитикам формировать диаграммы процессов

**Задачи:**
* Аналитик описывает процесс голосом
* Система генерирует диаграмму и отображает ее аналитику
* Система в режиме чата с аналитиком вносит правки в диаграмму

## Митапы и чек-пойнты 

### 04.04 Митап IT_ONE Cup. ML Challenge 

[Запись митапа](https://vk.com/video-201285708_456239164)

Небольшое резюие:
* Все модели, инструменты и готовые решения должны быть с лиценией open-source
* Финальное решение может быть MVP
* Инструменты должны идти в помощь аналитикам
* Можно посмотерть Communda, но с лицензией open-source
* Ожидается система, состоящая из нескольких моделей
* Для оценки решения будут использоваться кастомные метрики
* Упор на ядро решения, а не UI/UX

Резюме по треку BPMN:
* Процесс: аналиткик надиктовывает бизнес-процесс -> LLM рисует. Если аналиткиа не устроил результат, то он голосом вносит поправки
* Ожидается, что элементы диаграммы должны быть интеркативными (см. библиотеки x6, x7)
* Данные для обучения модели есть в Интеренете, их нужно немного
* Фронт для интерактивных элементов можно взять из Communda  

## Декомпозиция 

1. Найти open-source решения для транскрибации речи
2. Найти open-source модель для транскрибации речи
3. Найти и разметить корпус текстов по BPMN-диаграммам
4. Формализовать алгоритм создания диаграмм: понять, что выделяется в первую очередь, как устанавливать связи между объектами и т.д.

## User Stories 

1. Я как пользователь, хочу иметь возможность редактировать BPMN-диаграмму, чтобы вносить корректировки, не тратя лишнее время на перезапись описания процесса.
2. Я как пользователь, хочу видеть транскрибацию своего аудио, чтобы понять, какие команды поступают модели.
3. Я как пользователь, хочу иметь возможность вносить описание процесса текстом, чтобы создать BPMN-диаграмму, если у меня нет или не работает микрофон.
4. Я как пользователь, хочу иметь возможность описывать процессы не только через BPMN-диаграммы, чтобы иметь возможность описывать не только бизнес-процессы.
5. Я как пользователь, хочу видеть историю своих запросов, чтобы вернуться к редактированию запросов, созданных ранее.
6. Я как пользователь, хочу иметь возможность выбирать модель для генерации диаграмм, чтобы выбрать ту, которая точнее отображает процесс.
7. Я как пользователь, хочу иметь возможность выбирать, через какое устройство записывать мою речь, чтобы качество речи было лучше.
8. Я как пользовтаель, хочу иметь возможность редактирвать диагрмму, полученную не только при помощи голоса, но и из pdf и других форматов, чтобы вести описания процессов в этом инструменте.

## Use Cases

### Транскрибация речи

_Предусловие:_ устройство для записи речи ну опознано системой 

1. Система ищет устройства для записи речи.
2. Если устройства нет, то предлагает заполнить текстом. 


1. 

