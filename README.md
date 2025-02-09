# Exponential Smoothing and Time Series Analysis

## Описание проекта

В данном проекте проводится анализ временных рядов с использованием методов экспоненциального сглаживания (EMA). Основная цель — предсказать значения двух временных рядов и выбрать наиболее подходящую модель на основе метрик качества. Для анализа используются два временных ряда:

1. **Ежедневное количество рождений в Калифорнии (`daily-total-female-births-in-cal.csv`)**  
   Ряд стационарный, предсказание выполнено с помощью простого экспоненциального сглаживания (Single EMA).

2. **Ежемесячные вооружённые ограбления в Бостоне (`monthly-boston-armed-robberies-j.csv`)**  
   Ряд с трендом. Для него были применены два подхода:
   - Тройное экспоненциальное сглаживание (Triple EMA).
   - Двойное экспоненциальное сглаживание (Double EMA).  
   Выбор между методами основан на сравнении метрик качества.

## Содержимое репозитория

- `time_series_ema_analysis.ipynb` — Jupyter Notebook, содержащий весь процесс анализа, включая загрузку данных, визуализацию, выбор модели, кросс-валидацию и оценку метрик.
- `daily-total-female-births-in-cal.csv` — временной ряд с ежедневным количеством рождений в Калифорнии.
- `monthly-boston-armed-robberies-j.csv` — временной ряд с ежемесячными вооружёнными ограблениями в Бостоне.

## Используемые подходы

1. **Загрузка данных и предварительная обработка**:
   - Загрузка временных рядов через интерфейс Colab.
   - Проверка на стационарность с помощью теста Дики-Фуллера.
   - Преобразования данных, если это необходимо.

2. **Экспоненциальное сглаживание**:
   - **Single EMA** для стационарных рядов.
   - **Double EMA** для рядов с трендом.
   - **Triple EMA** для рядов с трендом и сезонностью.

3. **Кросс-валидация**:
   - Поиск оптимального параметра `alpha` для моделей EMA.

4. **Оценка качества**:
   - Использованы метрики: Средняя абсолютная ошибка (MAE) и Среднеквадратичная ошибка (MSE).

## Результаты

- **Daily Births in California**: Прогноз построен с использованием Single EMA, метрики показали высокую точность модели.
- **Boston Armed Robberies**:  
  - Прогноз с использованием Triple EMA оказался точнее, чем с Double EMA, подтверждая наличие тренда и сезонности.  
  - Double EMA также показал приемлемые результаты, но был менее точным.

## Установка и использование

1. Склонируйте репозиторий:
   ```bash
   git clone https://github.com/your_username/Exponential-Smoothing-Time-Series-Analysis.git



