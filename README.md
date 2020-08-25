# manipulator_trajectory_planning
## Описание
- Решение прямой и обратной задачи кинематики
- Планирование траектории движения
- Траекторное управление
- Моделирование процесса управления

## DH-параметры манипулятора
| Узел | a, cm | α, ° | d, cm | θ |
|:----:|:------:|:------------:|:------:|:-------:|
| 1 | 0 | 90 | 14 | θ1* |
| 2 | 12 | 0 | 0 | θ2* |
|3| 12 | 0 | 0 | θ3* |

## Прямая задача кинематики
Подставив DH пареметры манипулятора, получим три матрицы однородного преобразования:
![f1](https://latex.codecogs.com/gif.latex?T_i=\begin{bmatrix}cos(\theta)&-sin(\theta)cos(\alpha)&sin(\theta)sin(\alpha)&a\cdot\cos(\theta)\\sin(\theta)&cos(\theta)cos(\alpha)&-cos(\theta)sin(\alpha)&a\cdot\sin(\alpha)\\0&sin(\alpha)&cos(\alpha)&d\\0&0&0&1\end{bmatrix})

Итоговую матрицу получаем последовательным перемножением:
<img align="left" src="https://latex.codecogs.com/gif.latex?T=T_1\cdot\;T_2\cdot\;T_3=\begin{bmatrix}r_1_1&r_1_2&r_1_3&x\\r_2_1&r_2_2&r_2_3&y\\r_3_1&r_3_2&r_3_3&z\\0&0&0&1\end{bmatrix}">   


## Обратная задача кинематики

## Планирование траектории
Гармоническая траектория основанная на тригонометрических функциях имеет
следующую математическую формулировку:
s(θ)=R(1−cosθ) , 
где R – радиус окружности.
В более общем случае, гармоническая траектория может быть определена как

где q0, q1 – начальное и конечное значение угла поворота вала двигателя, t0, t1 - начальное и
конечное значение времени, t – текущее время, tp – время переходного процесса.
Продифференцировав представленное выражение по времени получим формулу для
угловой скорости вражения вала двигателя:

## Результаты

