# vk_test
Тестовое задания для стажировки в команде vk CoreML

Вопрос 1:
метрики для коллаборативных моделей: RMSE, nDCG. 
метрика для LightFM - ROC-AUC

Вопрос 2:
Трейн и тест для коллаборативных моделей я сделала по дате выбора. Для каждого пользователя посчитала 80% фильмов, которые он уже посмотрел, 20% оставила на проверку.  На трейне модели учились при помощи кросс-валидации с k=5
Для LightFM я воспользовалась встроенным разделением на тест и трейн


Вопрос 3:
Для SVD модели гиперпараметры не настраивались, для ALS и LightFM настраивались при помощи сетки

Вопрос 4:
Итоговые результаты моделей следующие:
 * SVD, RMSE: 0.926, nDCG: 0.968\
 * ALS, RMSE: 0.86, nDCG: 0.976\
 * LightFM, AUC-ROC: 0.998 (на трейне), 0.92 (на тесте)

Среди коллаборативных моделей выигрывает SVD. С точки зрения ранжирования она ошибается незначительно хуже, зато RMSE у нее выше на 6%. 
LightFM на тесте показала ROC-AUC 0.92, что является очень хорошим результатом. На мой взгляд, лучшие модели SVD и LightFM
