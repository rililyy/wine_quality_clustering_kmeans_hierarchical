# Использование методов иерархической кластеризации и алгоритма k-means для определения качества вина
Цель проекта -  применение указанных методов для определения качества вина на основе его физико-химических характеристик 

Исследование выполнено на основе открытого датасета о красном вине из Португалии.

Код программы написан на языке R. Также был создан дашборт в аналитической программе Glarus BI.

Методы:
- **KMeans кластеризация**
- **Иерархическая кластеризация** 

В рамках работы проводится:
- изучить теоретические основы методов кластеризации: иерархической кластеризации и алгоритма K-средних (K-means);
- провести исследовательский анализ данных (EDA);
- применить указанные алгоритмы кластеризации к обработанным данным;
- оценить и сравнить результаты кластеризации;
- визуализировать полученные кластеры и интерпретировать результаты анализа;
- создать дашборд с результатами в Glarus BI.


## Используемые библиотеки

- `dplyr`, `readr`
- `ggcorrplot`, `ggplot2`
- `cluster`, `mclust`
- `factoextra`

## Данные

Датасет (https://www.kaggle.com/datasets/uciml/red-wine-quality-cortez-et-al-2009)
содержит информацию о 1599 образцах красного португальского вина сорта Vinho Verde.

**Признаки:**
- fixed acidity - фиксированная кислотность (г/дм³)
- volatile acidity - летучая кислотность (г/дм³)
- citric acid - лимонная кислота (г/дм³)
- residual sugar - остаточный сахар (г/дм³)
- chlorides – содержание хлоридов (г/дм³)
- free sulfur dioxide - свободный диоксид серы (мг/дм³)
- total sulfur dioxide - общий диоксид серы (мг/дм³)
- density – плотность (г/дм³)
- pH
- sulphates - сульфаты
- alcohol – спирт
- quality качество (оценка от 0 до 10)

Целевая переменная quality представляет собой субъективную оценку, присвоенную экспертами на дегустациях.


## Краткий обзор результатов

- Проведена обработка данных - очистка от выбросов;
- Использован силуэтный метод и метод локтя для определения оптимального k;
- Сравнено распределение кластеров с фактическим качеством вина;
- Выполнена визуализация в пространстве PCA с границами кластеров;
- Создан дашборд в Glarus BI.


## Выводы
Несмотря на успешную реализацию алгоритмов и визуализацию полученных кластеров, с помощью методов кластеризации не удалось обнаружить устойчивую кластерную структуру, соответствующую целевой метке. Это указывает на ограниченность признакового пространства или сложную природу качества вина. Также не исключена сложная, многомерная природа оценки качества вина, которая может включать субъективные факторы и другие переменные, не представленные в используемом датасете.
Полученные выводы подчеркивают, что в задачах оценки качества вина одних лишь количественных характеристик может быть недостаточно, и для более точного анализа могут потребоваться либо дополнительные признаки, либо применение более сложных моделей машинного обучения с учётом целевой переменной, таких как модели случайного леса и д.р.
