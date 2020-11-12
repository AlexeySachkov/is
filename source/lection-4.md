<style type="text/css">
.reveal h1 {
  font-size: 2em;
}
.reveal .slides p {
  text-align: left;
}
</style>

# Интеллектуальные системы и технологии

---

## Распознавание изображений

----

### Распознавание образов

Образ - структурируемое описание изучаемого объекта или явления, представленное вектором признаков, каждый элемент которого представляет числовое значение одного из признаков, характеризующих соответствующий объект.

(тонкий, белый, легкий) - лист бумаги

(толстый, коричневый, тяжелый) - лист картона

----

![image](https://intuit.ru/EDI/22_02_16_6/1456093353-18215/tutorial/118/objects/4/files/4_1.gif)

----

Суть задачи распознавания - установить, обладают ли изучаемые объекты фиксированным конечным набором признаков, позволяющих отнести их к определенному классу.

----

### Особенности задач распознавания

- как правило задача состоит из 2-х этапов: (а) приведение данных к удобному виду, (б) само распознавание
- можно вводить понятие аналогии или подобия объектов и формулировать понятие близости объектов в качестве основания для зачисления объектов в один и тот же класс или разные классы

----

- можно оперировать набором готовых прецендентов-примеров, классификация которых уже известна и которые в виде формализованных описаний могут быть предъявлены алгоритму распознавания для настройки на задачу в процессе обучения
- трудно строить формальные теории и применять классические математические методы

----

- возможна "плохая" информация: пропуски информации, разнородная информация, нечеткая или косвенная информация

----

### Типы задач распознавания

- Задача распознавания - отнесение предъявленного объекта по его описанию к одному из заданных классов (обучение с учителем)
- Задача автоматической классификации - разбиение множества объектов по их описаниям на систему непересекающихся классов

----

- Задача выбора информативного набора признаков при классификации
- Первые две задачи для динамических объектов (видео)

---

## Основы теории анализа и распознавания образов

----

\begin{aligned}
M - множество\ объектов \\
\end{aligned}
\begin{aligned}
\Omega - множество\ классов\ объектов \\
\end{aligned}
\begin{aligned}
M = \bigcup \Omega_{i} (i=1..m) \\
\end{aligned}
\begin{aligned}
Каждый\ объект\ w_{i}
\end{aligned}
\begin{aligned}
задается\ значениями\ признаков\ x_{j} (j=1..N) \\
\end{aligned}
\begin{aligned}
I(w)=(x_{1}(w),...,x_{N}(w)) - описание\ объекта
\end{aligned}

----

#### Таблица обучения

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:24px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:24px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
</style>
<table class="tg">
<thead>
  <tr>
    <th class="tg-0pky" rowspan="2">объект</th>
    <th class="tg-0pky" colspan="3">признаки и значения</th>
    <th class="tg-0pky" rowspan="2">класс</th>
  </tr>
  <tr>
    <td class="tg-0pky">
        \begin{aligned}
        x_{1}
        \end{aligned}
    </td>
    <td class="tg-0pky">
        \begin{aligned}
        x_{j}
        \end{aligned}
    </td>
    <td class="tg-0pky">
        \begin{aligned}
        x_{n}
        \end{aligned}
    </td>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0pky">
        \begin{aligned}
        w_{1}
        \end{aligned}
    </td>
    <td class="tg-0pky">
        \begin{aligned}
        a_{11}
        \end{aligned}
    </td>
    <td class="tg-0pky">
        \begin{aligned}
        a_{1j}
        \end{aligned}
    </td>
    <td class="tg-0pky">
        \begin{aligned}
        a_{1n}
        \end{aligned}
    </td>
    <td class="tg-0pky" rowspan="3">
        \begin{aligned}
        \Omega_{1}
        \end{aligned}
    </td>
  </tr>
  <tr>
    <td class="tg-0pky" colspan="4">...</td>
  </tr>
  <tr>
    <td class="tg-0pky">
        \begin{aligned}
        w_{h}
        \end{aligned}
    </td>
    <td class="tg-0pky">
        \begin{aligned}
        a_{h1}
        \end{aligned}
    </td>
    <td class="tg-0pky">
        \begin{aligned}
        a_{hj}
        \end{aligned}
    </td>
    <td class="tg-0pky">
        \begin{aligned}
        a_{hn}
        \end{aligned}
    </td>
  </tr>
  <tr>
    <td class="tg-0pky" colspan="5">...</td>
  </tr>
  <tr>
    <td class="tg-0pky">
        \begin{aligned}
        w_{l}
        \end{aligned}
    </td>
    <td class="tg-0pky">
        \begin{aligned}
        a_{l1}
        \end{aligned}
    </td>
    <td class="tg-0pky">
        \begin{aligned}
        a_{lj}
        \end{aligned}
    </td>
    <td class="tg-0pky">
        \begin{aligned}
        a_{ln}
        \end{aligned}
    </td>
    <td class="tg-0pky" rowspan="3">
        \begin{aligned}
        \Omega_{M}
        \end{aligned}
    </td>
  </tr>
  <tr>
    <td class="tg-0pky" colspan="4">...</td>
  </tr>
  <tr>
    <td class="tg-0pky">
        \begin{aligned}
        w_{k}
        \end{aligned}
    </td>
    <td class="tg-0pky">
        \begin{aligned}
        a_{k1}
        \end{aligned}
    </td>
    <td class="tg-0pky">
        \begin{aligned}
        a_{kj}
        \end{aligned}
    </td>
    <td class="tg-0pky">
        \begin{aligned}
        a_{kn}
        \end{aligned}
    </td>
  </tr>
</tbody>
</table>

----

Имея описание нового объекта
\begin{aligned}
A=(a_{1},...,a_{N})
\end{aligned}
И описание какого-то уже существующего объекта
\begin{aligned}
B=(b_{1},...,b_{N})
\end{aligned}

Мы можем попытаться понять, похожи они или нет

----

\begin{aligned}
\varepsilon_{1},...,\varepsilon_{N} - пороги\ несоотвествия\ для\ каждого\ признака
\end{aligned}

Если хотя бы q неравенств выполнаются, то объекты считаются принадлежащими одному классу:
\begin{aligned}
\mid a_{i} - b_{i} \mid \eqslantless \varepsilon_{i}, i = (1...N)
\end{aligned}

----

#### Пример

![Numbers](https://i.imgur.com/c3qp7DE.png)

----

1. Количества вертикальных линий (длины 1)
2. Количество горизонтальных линий
3. Количество наклонных линий

----

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:24px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:24px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax">
        \begin{aligned}
        X_{1}
        \end{aligned}
    </th>
    <th class="tg-0lax">
        \begin{aligned}
        X_{2}
        \end{aligned}
    </th>
    <th class="tg-0lax">
        \begin{aligned}
        X_{3}
        \end{aligned}
    </th>
    <th class="tg-0lax"></th>
    <th class="tg-0lax"></th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">4</td>
    <td class="tg-0lax">2</td>
    <td class="tg-0lax">0</td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax">0</td>
  </tr>
  <tr>
    <td class="tg-0lax">2</td>
    <td class="tg-0lax">0</td>
    <td class="tg-0lax">1</td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax">1</td>
  </tr>
  <tr>
    <td class="tg-0lax">1</td>
    <td class="tg-0lax">2</td>
    <td class="tg-0lax">1</td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax">2</td>
  </tr>
  <tr>
    <td class="tg-0lax">0</td>
    <td class="tg-0lax">2</td>
    <td class="tg-0lax">2</td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax">3</td>
  </tr>
  <tr>
    <td class="tg-0lax">3</td>
    <td class="tg-0lax">1</td>
    <td class="tg-0lax">0</td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax">4</td>
  </tr>
  <tr>
    <td class="tg-0lax">2</td>
    <td class="tg-0lax">3</td>
    <td class="tg-0lax">0</td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax">5</td>
  </tr>
  <tr>
    <td class="tg-0lax">2</td>
    <td class="tg-0lax">2</td>
    <td class="tg-0lax">1</td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax">6</td>
  </tr>
  <tr>
    <td class="tg-0lax">1</td>
    <td class="tg-0lax">1</td>
    <td class="tg-0lax">1</td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax">7</td>
  </tr>
  <tr>
    <td class="tg-0lax">4</td>
    <td class="tg-0lax">3</td>
    <td class="tg-0lax">0</td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax">8</td>
  </tr>
  <tr>
    <td class="tg-0lax">2</td>
    <td class="tg-0lax">2</td>
    <td class="tg-0lax">1</td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax">9</td>
  </tr>
  <tr>
    <td class="tg-0lax">
        \begin{aligned}
        \varepsilon_{1}=1
        \end{aligned}
    </td>
    <td class="tg-0lax">
        \begin{aligned}
        \varepsilon_{2}=1
        \end{aligned}
    </td>
    <td class="tg-0lax">
        \begin{aligned}
        \varepsilon_{3}=1
        \end{aligned}
    </td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax"></td>
  </tr>
</tbody>
</table>

----

![Numbers](https://i.imgur.com/c3qp7DE.png)

----

4. Количество горизонтальных линий снизу объекта

----

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax">
        \begin{aligned}
        X_{1}
        \end{aligned}
    </th>
    <th class="tg-0lax">
        \begin{aligned}
        X_{2}
        \end{aligned}
    </th>
    <th class="tg-0lax">
        \begin{aligned}
        X_{3}
        \end{aligned}
    </th>
    <th class="tg-0lax"></th>
    <th class="tg-0lax"></th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">4</td>
    <td class="tg-0lax">2</td>
    <td class="tg-0lax">0</td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax">0</td>
  </tr>
  <tr>
    <td class="tg-0lax">2</td>
    <td class="tg-0lax">0</td>
    <td class="tg-0lax">1</td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax">1</td>
  </tr>
  <tr>
    <td class="tg-0lax">1</td>
    <td class="tg-0lax">2</td>
    <td class="tg-0lax">1</td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax">2</td>
  </tr>
  <tr>
    <td class="tg-0lax">0</td>
    <td class="tg-0lax">2</td>
    <td class="tg-0lax">2</td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax">3</td>
  </tr>
  <tr>
    <td class="tg-0lax">3</td>
    <td class="tg-0lax">1</td>
    <td class="tg-0lax">0</td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax">4</td>
  </tr>
  <tr>
    <td class="tg-0lax">2</td>
    <td class="tg-0lax">3</td>
    <td class="tg-0lax">0</td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax">5</td>
  </tr>
  <tr>
    <td class="tg-0lax">2</td>
    <td class="tg-0lax">2</td>
    <td class="tg-0lax">1</td>
    <td class="tg-0lax">1</td>
    <td class="tg-0lax">6</td>
  </tr>
  <tr>
    <td class="tg-0lax">1</td>
    <td class="tg-0lax">1</td>
    <td class="tg-0lax">1</td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax">7</td>
  </tr>
  <tr>
    <td class="tg-0lax">4</td>
    <td class="tg-0lax">3</td>
    <td class="tg-0lax">0</td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax">8</td>
  </tr>
  <tr>
    <td class="tg-0lax">2</td>
    <td class="tg-0lax">2</td>
    <td class="tg-0lax">1</td>
    <td class="tg-0lax">0</td>
    <td class="tg-0lax">9</td>
  </tr>
  <tr>
    <td class="tg-0lax">
        \begin{aligned}
        \varepsilon_{1}=1
        \end{aligned}
    </td>
    <td class="tg-0lax">
        \begin{aligned}
        \varepsilon_{2}=1
        \end{aligned}
    </td>
    <td class="tg-0lax">
        \begin{aligned}
        \varepsilon_{3}=1
        \end{aligned}
    </td>
    <td class="tg-0lax">
        \begin{aligned}
        \varepsilon_{4}=1
        \end{aligned}
    </td>
    <td class="tg-0lax"></td>
  </tr>
</tbody>
</table>

----

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:24px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:24px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax">
        \begin{aligned}
        X_{1}
        \end{aligned}
    </th>
    <th class="tg-0lax">
        \begin{aligned}
        X_{2}
        \end{aligned}
    </th>
    <th class="tg-0lax">
        \begin{aligned}
        X_{3}
        \end{aligned}
    </th>
    <th class="tg-0lax">
        \begin{aligned}
        X_{4}
        \end{aligned}
    </th>
    <th class="tg-0lax">Объект</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">1</td>
    <td class="tg-0lax">2</td>
    <td class="tg-0lax">1</td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax">№1</td>
  </tr>
  <tr>
    <td class="tg-0lax">3</td>
    <td class="tg-0lax">3</td>
    <td class="tg-0lax">0</td>
    <td class="tg-0lax">1</td>
    <td class="tg-0lax">№2</td>
  </tr>
  <tr>
    <td class="tg-0lax">4</td>
    <td class="tg-0lax">1</td>
    <td class="tg-0lax">0</td>
    <td class="tg-0lax"></td>
    <td class="tg-0lax">№3</td>
  </tr>
  <tr>
    <td class="tg-0lax">4</td>
    <td class="tg-0lax">2</td>
    <td class="tg-0lax">0</td>
    <td class="tg-0lax">1</td>
    <td class="tg-0lax">№4</td>
  </tr>
  </tr>
</tbody>
</table>

----

![Numbers](https://i.imgur.com/c3qp7DE.png)

----

