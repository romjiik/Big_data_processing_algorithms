# Big_data_processing_algorithms
HSE course of big data processing algorithms

В данном курсе были разобраны основы работы с hdfs, hive, PySpark и смежных библиотек для обучения ML-моделей

Было выполнено 2 проекта:
1. Решить 5 аналитических задач с помощью Apache Spark SQL
2. По данным постов в телеграм каналах предсказать количество просмотров этих постов. Feature engineering реализован полносью на PySpark. Модель для предсказания - catboost 
    * Данные.
      Предоставляется 3 файла:
      1. трейн сет (с количеством просмотров)
      2. тест сет (без количества просмотров)
      3. метаданные каналов
      Трейн и тест разбиты по времени. Как прочитать данные можно посмотреть в ноутбуке.
    * Задание.
      1. Подсчитать фичи для модели, используя только Spark
      2. Фичи можно перевести в pandas и обучить свой любимый алгоритм локально (но не обязательно)
      3. Предсказать им тест сет и побить бейзлайн по целевым метрикам
    * Метрики.
      Поскольку просмотры распределены экспоненциально, предсказывать будем странную величину log(post_views + 100). Вычисляются      сразу 4 метрики, но они связаны между собой. Это
      RMSPE - Root Mean Squared Percentage Error
      MAPE - Mean Absolute Percentage Error
      MAE - Mean Absolute Error
      RMSE - Root Mean Squared Error

