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

---

## Обучение и работа нейронной сети

----

### Метод обратного распространения ошибки

----

![image](https://neurohive.io/wp-content/uploads/2018/07/forward-propagation-570x570.png)

----

![image](https://neurohive.io/wp-content/uploads/2018/07/backpropagation-770x372.jpeg)

----

