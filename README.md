# SberAuto-Insights
# Итоговый проект: Анализ сайта "СберАвтоподписка"

## Описание проекта
Этот проект представляет собой анализ данных веб-сайта "СберАвтоподписка" с целью извлечения полезных инсайтов, оценки поведения пользователей и разработки моделей предсказания их действий. 

## Цели проекта
- Провести разведочный анализ данных (EDA);
- Проверить и оценить статистические гипотезы;
- Разработать предсказательную модель для совершения целевого действия пользователями;
- Реализовать процесс обработки данных и их хранения;
- Подготовить презентацию с результатами анализа.

## Данные
В проекте используются данные из Google Analytics (last-click attribution model):
- `GA Sessions (ga_sessions.pkl)`: одна строка = один визит на сайт.
- `GA Hits (ga_hits.pkl)`: одна строка = одно событие в рамках одного визита на сайт.

### Основные атрибуты данных:
- **session_id** — ID визита;
- **client_id** — ID посетителя;
- **visit_date, visit_time** — дата и время визита;
- **utm_source, utm_medium, utm_campaign** — источник и параметры трафика;
- **device_category, device_os, device_brand** — устройство пользователя;
- **geo_country, geo_city** — география пользователя;
- **event_action, event_label** — действия пользователя на сайте.

## Выполняемые задачи
### 1. Разведочный анализ данных (EDA)
- Очистка данных (удаление дубликатов, обработка пропущенных значений);
- Анализ распределений ключевых признаков;
- Выявление корреляций между параметрами.

### 2. Проверка статистических гипотез (DA)
- Сравнение конверсии (CR) для различных типов трафика (органический vs. платный);
- Анализ различий в конверсии между мобильными и десктопными пользователями;
- Оценка эффективности рекламы в соцсетях.

### 3. Разработка ML-модели (ML)
- Подготовка данных и фиче-инжиниринг;
- Обучение модели предсказания целевого действия (ROC-AUC ~ 0.83);
- Реализация API для предсказания действий пользователей.

### 4. Разработка базы данных и пайплайна обработки данных (DE)
- Настройка базы данных и схемы хранения данных;
- Автоматизация загрузки новых данных с использованием Airflow;
- Оптимизация запросов и мониторинг работы системы.

## Используемые технологии
- **Язык программирования:** Python (Jupyter Notebook, .py-скрипты);
- **Библиотеки:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Statsmodels;
- **Работа с базами данных:** SQL, PostgreSQL;
- **Автоматизация:** Apache Airflow;
- **API:** FastAPI или Flask (для ML-модели).




