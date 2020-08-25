# manipulator_trajectory_planning
## Описание
- Решение прямой и обратной задачи кинематики
- Планирование траектории движения
- Траекторное управление
- Моделирование процесса управления

## DH-параметры манипулятора
| Узел | a, cm | $\alpha$, ° | d, cm | \theta |
|:----:|:------:|:------------:|:------:|:-------:|
| 1 | 0 | 90 | 14 | \theta1* |
| 2 | 12 | 0 | 0 | \theta2* |
|3| 12 | 0 | 0 | \theta3* |

## Прямая задача кинематики
Матрицы однородного преобразования:

<img align="left" src="https://latex.codecogs.com/gif.latex?T=\begin{bmatrix}cos(\theta)&-sin(\theta)cos(\alpha)&sin(\theta)sin(\alpha)&a\cdot\cos(\theta)\\sin(\theta)&cos(\theta)cos(\alpha)&-cos(\theta)sin(\alpha)&a\cdot\sin(\alpha)\\0&sin(\alpha)&cos(\alpha)&d\\0&0&0&1\end{bmatrix}" /> 

Итоговую матрицу получаем последовательным перемножением:


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

