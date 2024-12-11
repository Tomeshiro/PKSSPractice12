# PKSSPractice12

## Mindmap

Здесь представлены ключевые особенности нашей информационной системы

```mermaid
mindmap
Информационная система
	Пользователи
		Авторы
		Переводчики
		Читатели
	Архитектура
		Шаблоны проектирования
			Адаптер
			Наблюдатель
			Состояние
			Одиночка
		Микросервисы
			Контроллер
			Работы с клиентами
			Работы с произведениями
			Работы с грамматическим ИИ
			Работы с машинным переводчиком
			Репозиторий
		Внешние системы
			Машинный переводчик
			ИИ проверки грамматики
			Облачная база данных
	Технологии
		Backend
			Java
			Spring Framework
			MongoDB
		Frontend
			JavaScript
			React
	Функции
		Покупать произведения
		Читать произведения
		Продавать произведения
		Переводить произведения

```

## User Journey Diagram

Здесь представлен путь пользователя

```mermaid
journey
    title Общий путь пользователя в информационной системе
    section Вход в систему
      Зарегистрироваться: 5: Читатель
      Войти в аккаунт: 3: Читатель
      Сверить данные: 3: Сервер
    section Просмотр глав
      Ввести название произведения: 5: Читатель
      Найти данное произведение в БД: 3: Сервер
      Показать данное произведение: 4: Клиент
	section Покупка глав
	  Купить данное произведение: 5: Читатель
	  Обработать покупку: 4: Сервер
	  Дать доступ к главе: 3: Сервер
	  Отобразить главу: 4: Клиент
	section Завершение сессии
	  Завершение чтения: 5: Читатель
	  Сохранить информацию о прочитанных главах: 4: Сервер
	  Завершение сеанса: 3: Читатель
	  Выход из системы: 3: Читатель
```
## Квадрант-граф

Здесь представлен квадрант-граф

```mermaid
quadrantChart
    title Приоритеты разработки функционала
    x-axis "Низкий приоритет" --> "Высокий приоритет"
    y-axis "Низкая сложность" --> "Высокая сложность"
    quadrant-1 "Реализовать немедленно"
    quadrant-2 "Планировать в ближайшее время"
    quadrant-3 "Возможно, стоит отказаться"
    quadrant-4 "Требует тщательного анализа"
    "Механизм покупки глав": [0.9, 0.6]
    "Авторизация": [0.85, 0.4]
    "Регистрация": [0.95, 0.3]
    "Механизм публикации глав": [0.95, 0.8]
    "Интеграция машинного переводчика": [0.65, 0.9]
    "Интеграция грамматического ИИ": [0.45, 0.7]
    "Чат между переводчиком и автором": [0.3, 0.8]
    "Отзывы о произведениях": [0.2, 0.6]
    "Отзывы о произведениях": [0.2, 0.6]
    "Сохранение кол-ва прочитанных глав": [0.75, 0.25]
    "Уведомление о новой главе": [0.2, 0.2]
    "Смена пароля": [0.4, 0.4]
```

## GitGraph

Так выглядит наш примерный путь коммитов

```mermaid
---
title: Git diagram for translator's system
---
gitGraph
   commit id: "Start"
   branch develop
   checkout develop
   commit id: "Start develop"
   branch ClientMicroservice
   commit id: "Client Service creation"
   checkout develop
   merge ClientMicroservice
   commit id: "Client Service integration"
   branch ChapterMicroservice
   commit id: "Chapter service creation"
   checkout develop
   merge ChapterMicroservice
   commit id: "Chapter service integration"
   branch WritingMicroservice
   commit id: "Writing service creation"
   checkout develop
   merge WritingMicroservice
   commit id: "Writing service integration"
   branch MachineTranslatorMicroservice
   commit id: "Machine translation service creation"
   checkout develop
   merge MachineTranslatorMicroservice
   commit id: "Machine creation service integration"
   branch GrammarMicroservice
   commit id: "Grammar service creation"
   checkout develop
   merge GrammarMicroservice
   commit id: "Grammar service integration"
   checkout main
   merge develop
   commit id: "First version"
```
