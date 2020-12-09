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
V_{i} = f(V_{j}, \omega_{j}, h_{j})
\end{aligned}
\begin{aligned}
f(V_{j}, \omega_{j}, h_{j}) = \sum_j k_{j} \\
\end{aligned}
\begin{aligned}
k_{j} = V_{j} * \omega_{j},\ if\ V_{j} * \omega_{j} > h_{j}\ or\ 0\ otherwise
\end{aligned}

----

\begin{aligned}
V_{i} = f(V_{j}, \omega_{j}, h_{j}) \\
\end{aligned}
\begin{aligned}
f(V_{j}, \omega_{j}, h_{j}) = \sum_j V_{j} * \omega_{j} - h_{j}
\end{aligned}

----

\begin{aligned}
V_{i} = f(V_{j}, \omega_{j}, h_{j}) \\
\end{aligned}
\begin{aligned}
f(V_{j}, \omega_{j}) = V_{0_{j}} * \omega_{0_{j}} + \sum_j V_{j} * \omega_{j}
\end{aligned}

----

\begin{aligned}
D(f) = [0, 1]
\end{aligned}

----

![image](https://neerc.ifmo.ru/wiki/images/thumb/6/63/Multi-layer-neural-net-scheme.png/500px-Multi-layer-neural-net-scheme.png)

----

![image](http://synset.com/ai/ru/nn/im/nets01.png)

----

![image](http://synset.com/ai/ru/nn/im/nets02.png)