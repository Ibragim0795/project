# Yandex praktikum Projects
# Отток клиентов
Описание проекта
Из «Бета-Банка» стали уходить клиенты. Каждый месяц. Немного, но заметно. Банковские маркетологи посчитали: сохранять текущих клиентов дешевле, чем привлекать новых.
Нужно спрогнозировать, уйдёт клиент из банка в ближайшее время или нет.

# Описание данных
- RowNumber — индекс строки в данных
- CustomerId — уникальный идентификатор клиента
- Surname — фамилия
- CreditScore — кредитный рейтинг
- Geography — страна проживания
- Gender — пол
- Age — возраст
- Tenure — количество недвижимости у клиента
- Balance — баланс на счёте
- NumOfProducts — количество продуктов банка, используемых клиентом
- HasCrCard — наличие кредитной карты
- IsActiveMember — активность клиента
- EstimatedSalary — предполагаемая зарплата
- Exited — Целевой признак, факт ухода клиента

# Итоговые выводы

- В первоначальные данных был дисбаланс. 80% / 20%. Из-за этого обученная на этих данных модель не проходила проверку на адекватность. Все модели на первоначальных данных были с высокой степенью ошибок и низким качеством взвешенной величины (F1). Модели показывали низкую точность и полноту.


- Убрал дисбаланс классов в обучающей выборке. Увеличил количество значений позитивного класса в 4 раза. Так был достигнут баланс классов в обучеющей выборке: 0 - 0.501043 1 - 0.498957


- Разобрали несколько вариантов борьбы с дисбалансом upsampling и downsampling


- На новых данных все модели показали результат выше, чем на несбалансированной выборке. Лучшие показатели были у модели случайного леса.
        -Полнота 0.722488038277512
        -Точность 0.5392857142857143
        -F1-мера 0.6175869120654396
        -AUC-ROC 0.8527604207622839

- Финальная модель прошла проверку на адекватность в сравнении с контантной моделью: accuracy_score константой модели: 0.796
        -aaccuracy_score константой модели: 0.791
        -accuracy_score финальной модели: 0.8015
        -AUC-ROC константой модели: 0.5
        -AUC-ROC финальной модели: 0.8513006861338599
