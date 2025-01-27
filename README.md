Жақсыбай Бақтияр

Так как перед нами стоит задача бинарной классификации, какую функцию потерь лучше всего применить в нашем случае?

•	бинарная кросс-энтропия (binary crossentropy)

Примечание: Если вы используете активацию для выходного слоя, не требуется устанавливать from_logits=True.


Вопрос 2
Определите общее количество параметров в модели. Для этого примените метод summary.
•	11215873
Генераторы и обучение
Для следующих двух вопросов используйте следующий генератор данных для обучающих (train) и тестовых (test) наборов:
ImageDataGenerator(rescale=1./255)
Примечание: Дополнительная предобработка изображений не требуется. При загрузке данных из каталогов обучения/тестирования убедитесь, что параметр class_mode установлен правильно для задачи бинарной классификации. Рекомендуемые параметры: batch_size=20 и shuffle=True.
Для обучения примените метод .fit() со следующими параметрами:
model.fit( train_generator, epochs=10, validation_data=test_generator)


Вопрос 3
Какова медиана точности обучения по всем эпохам?

Медиана точности обучения: 0.90

Вопрос 4
Каково стандартное отклонение потерь в процессе обучения по всем эпохам?

Стандартное отклонение потерь: 0.09


Аугментация данных
Для следующего этапа вам потребуется генерировать больше данных с помощью аугментаций.
Добавьте следующие аугментации к генератору обучающих данных:
rotation_range=40,
width_shift_range=0.2,
height_shift_range=0.2,
shear_range=0.2,
zoom_range=0.2,
horizontal_flip=True,
fill_mode='nearest'



Вопрос 5 и  6
Обучите модель еще на 10 эпох с использованием указанного выше кода. Не создавайте модель с нуля; продолжите обучение существующей.
Каково среднее значение потерь на тестовом наборе данных по всем эпохам после аугментации?

Каково среднее значение точности на тестовом наборе данных за последние 5 эпох (с 6 по 10) после аугментации?

Общее количество параметров в модели: 11215873
Среднее значение потерь после аугментации: 0.42
Средняя точность за последние 5 эпох: 0.82
![image](https://github.com/Baktiyar88/SRO---/assets/158766882/e43cd53b-235c-4ab4-be4b-502d9989703c)


![image](https://github.com/Baktiyar88/SRO---/assets/158766882/fc2f2d82-feeb-4ae3-bce4-4eaf98d11675)
![image](https://github.com/Baktiyar88/SRO---/assets/158766882/79c49832-fbf4-4baf-8062-38b397890861)

![image](https://github.com/Baktiyar88/SRO---/assets/158766882/cec51ce7-fe85-4a5b-93a6-ae8b2464d8e0)
![image](https://github.com/Baktiyar88/SRO---/assets/158766882/f324a112-ecdf-4ad9-9a06-614555e07a6e)

![image](https://github.com/Baktiyar88/SRO---/assets/158766882/aeca8af2-2e15-4d23-ac8f-3a0ce7bc8f5d)
![image](https://github.com/Baktiyar88/SRO---/assets/158766882/2c970024-ff27-49c3-8078-d09d1cbcc5da)

![image](https://github.com/Baktiyar88/SRO---/assets/158766882/fc983705-f758-4661-b86c-0901a87dfd67)
![image](https://github.com/Baktiyar88/SRO---/assets/158766882/7778a135-39cb-461f-b892-1d5a14c55b90)

