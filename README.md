# Задача на практику: классификация эмоций по русифицированному датасету ru_go_emotions и достижение точности 90%

Датасет был взят с платформы HugginFace, где были русифицированные метки и предложения. Очистка текста производилось методами бибилиотек pymorphy2 и nltk.
В исследовании были проверены разные методы векторизации данных: bag of word, Word2Vec, BERT, Keras embedding, а также модели построенные с использованием разных слоёв: Dense, LSTM, CONV1D и MaxPooling, SimpleRNN и GRU
В исследовании лучше всего себя показали Keras Embedding в сочетании с моделью из LSTM слоёв, однако результат был 50% точности, что далеко от поставленной задачи.

После этого было принято решение использовать LLM (крупные языковые модели) для полного решения задачи классификации, а не только векторизации, как раньше. Исследование проводилось на RuBERT и LaBSE моделях.
