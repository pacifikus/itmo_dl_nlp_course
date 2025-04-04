### Домашнее задание 4 - 10 баллов

В этом задании вам предстоит дообучить трансформерную модель для NER-задачи в различных форматах:

1. Обучите NER-модель

- Загрузите набор данных [Collection5](https://github.com/natasha/corus?tab=readme-ov-file#load_ne5) - **1 балл**
- Разбейте набор данных на train/test части
- Дообучите модель [rubert-tiny2](https://huggingface.co/cointegrated/rubert-tiny2) на train-части корпуса для решения NER-задачи, сделайте замеры качества NER-метрик до и после дообучения - **2 балла**

2. Попробуйте улучшить качество модели следующими способами:
- Предварительно дообучите на train-части в MLM режиме, а потом дообучите на NER-задачу - **2 балла**
- Сгенерируйте синтетическую разметку* подходящего**, на ваш взгляд, новостного корпуса большой и умной моделью для русскоязычного NER***, а затем использовав ее для дообучения rubert-tiny2 вместе с основным набором данных - **2 балла**

3. Финально сравните результаты различных подходов - **1 балл**

*прогоните датасет через NER-модель, получите ее предсказания и используйте их в качестве резметки

**Можно использовать уже знакомый вам датасет lenta-ru, объем данных лучше взять от 10_000 текстов

***Например, можно взять модель модель DeepPavlov ner_collection3_bert. Инструкция по запуску есть в [документации](https://docs.deeppavlov.ai/en/master/features/models/NER.html)

**Общее**

- Принимаемые решения обоснованы (почему выбрана определенная архитектура/гиперпараметр/оптимизатор/преобразование и т.п.) - **1 балл**
- Обеспечена воспроизводимость решения: зафиксированы random_state, ноутбук воспроизводится от начала до конца без ошибок - **1 балл**

**Формат сдачи ДЗ**

- Каждая домашняя работа – PR в отдельную ветку **hw_n**, где **n** - номер домашней работы
- Добавить ментора и pacifikus в reviewers
- Дождаться ревью, если все ок – мержим в main
- Если не ок – вносим исправления и снова отправляем на ревью
