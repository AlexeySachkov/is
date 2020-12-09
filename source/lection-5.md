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
k_{j} = V_{j} * \omega_{j}, if V_{j} * \omega_{j} > h_{j} or 0 otherwise
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
f(V_{j}, \omega_{j}) = V_0 * \omega_0 + \sum_j V_{j} * \omega_{j}
\end{aligned}