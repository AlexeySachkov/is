<style type="text/css">
.reveal h1 {
  font-size: 2em;
}
</style>

# Интеллектуальные системы и технологии

---

## Нейронные сети

---

## Модель мозга

----

![image](https://intuit.ru/EDI/19_07_20_1/1595110787-29918/tutorial/641/objects/1/files/1-1.jpg)

----


### Математическая модель нейрона

![image](https://intuit.ru/EDI/19_07_20_1/1595110787-29918/tutorial/641/objects/1/files/1-2.jpg)

----


\begin{aligned}
D(f) = [0, 1]
\end{aligned}

----

\begin{aligned}
V_{i} = f(\sum_k V_{k} * \omega_{ik}, h_{i})
\end{aligned}
\begin{aligned}
f(Sum, h) = 1,\ if\ Sum > h\ or\ 0\ otherwise
\end{aligned}

----

\begin{aligned}
V_{i} = V_{i} = f(\sum_k V_{k} * \omega_{ik}, h_{i})
\end{aligned}
\begin{aligned}
f(Sum, h) = \sigma(Sum - h) = \frac{1}{1+e^{Sum - h}}
\end{aligned}

----

\begin{aligned}
V_{i} = V_{i} = f(\sum_k V_{k} * \omega_{ik}, h_{i})
\end{aligned}
\begin{aligned}
f(Sum, h) = \tanh(Sum - h)
\end{aligned}

----

![image](https://neurohive.io/wp-content/uploads/2018/07/funkcii-aktivacii-neironnoi-seti-570x257.png)

----

![image](https://neerc.ifmo.ru/wiki/images/thumb/6/63/Multi-layer-neural-net-scheme.png/500px-Multi-layer-neural-net-scheme.png)

----

![image](http://synset.com/ai/ru/nn/im/nets01.png)

----

![image](http://synset.com/ai/ru/nn/im/nets02.png)

----

![image](https://intuit.ru/EDI/19_07_20_1/1595110787-29918/tutorial/641/objects/2/files/2-1.jpg)

----

![image](https://intuit.ru/EDI/19_07_20_1/1595110787-29918/tutorial/641/objects/2/files/2-2.jpg)

----

![image](https://intuit.ru/EDI/19_07_20_1/1595110787-29918/tutorial/641/objects/2/files/2-3.jpg)

---

## Обучение и работа нейронной сети

----

### Метод обратного распространения ошибки

----

![image](https://neurohive.io/wp-content/uploads/2018/07/forward-propagation-570x570.png)

----

![image](https://neurohive.io/wp-content/uploads/2018/07/backpropagation-770x372.jpeg)

----

### Виды обучения нейросетей

- обучение с учителем
- обучение без учителя
- обучение с подкреплением

----

### Переобучение

Нейронная сеть "запоминает" ответы, вместо того, чтобы искать закономерности.

- регуляризация весов
- нормализация батчей
- наращивание обучающей выборки

----

### Катастрофическая забывчивость

Нельзя просто так обучить нейронную сеть решать вторую задачу:
веса нейронов будут переписаны и весь опыт для решения первой задачи будет забыт

---

## Виды нейронных сетей

----

### Feed Forward Neural Networks (FFNN)

Нейронные сети прямого распространения

![image](https://s3.tproger.ru/uploads/2016/09/1-3-300x88.png)

----

### Autoencoder (AE)

Автоматическое сжатие информации

![image](https://s3.tproger.ru/uploads/2016/09/7-1-222x300.png)

----

### Convolutional Neural Networks (CNN)

Сверточные нейронные сети

![image](https://s3.tproger.ru/uploads/2016/09/12-1-300x185.png)

----

### Deconvolutional Networks (DN)

Развертывающие нейронные сети

![image](https://s3.tproger.ru/uploads/2016/09/13-297x300.png)

---

## Средства для работы с нейронными сетями

----

### Tensorflow

An end-to-end open source machine learning platform

- https://www.tensorflow.org/

![image](https://miro.medium.com/max/700/1*e9sg7-4A6rCAsUek_VAgSA.gif)

----

### Keras

Simple. Flexible. Powerful. Deep learning for humans.

- https://keras.io/

----

### PyTorch

FROM RESEARCH TO PRODUCTION

- https://pytorch.org/
