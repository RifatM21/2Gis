Есть датасет.
Собран он следующим образом:

- Из логов были взяты пары ([запрос] - [объект на который кликнул пользователь]). Это положительные примеры (метка 1 в датасете)
- Для каждого запроса был подобран в пару негативный объект (метка 0) следующим образом: определяем к какой рубрике относится положительный пример; выбираем случайный объект из другой рубрики. Идея в том, что этот пример маловероятно будет релевантным.

На этих данных, используя кросс-валидацию, обучались различные модели. Метрики качества были хорошими.
При попытки тестирования на реальных данных, качество моделей сильно уступало тестовым метрикам.

Задача: выявить особенности датасета, которые приводили к данным результатам и объяснить почему так происходило.
