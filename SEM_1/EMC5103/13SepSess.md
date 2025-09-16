# 13 September 2025

[Click here for recording](https://cciitpatna-my.sharepoint.com/:v:/r/personal/emc5103_iitp_ac_in/Documents/Recordings/EMC%205103%20-%20Lecture%20Room-20250913_163540-Meeting%20Recording.mp4?csf=1&web=1&e=eaicgA&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D)

## Random variable

- Previously we discussed about random experiment, where we were concerned about the outcomes and number assocaited with it
- R.V is simply a function from sample space to real number
- R.V is a function with domain S and range {-$\infty$, +$\infty$} such that for every real number _a_ the event

## Results of RV

- A function X(w) from Sample _S_ to RV {-$\infty$, +$\infty$} is a RV,iff for for real a = {w : X(w) < a } belogs to _B_
- If X1 and X2 is RV then-
  - max {X1, X2} is also RV
  - min {X1, X2} is also RV
  - |X| is also RV
- If X is a RV then f(.) __f of that function__ is a continous/ increasing function then f(X) is also RV

## Types of random variable

- Discrete RV
  - A variable which can real value on a discrete sample space is called DRV
  - For eg. marks obtained in exam, number of accidents per month
  - Probability mass function and Probability density function

  - PMF
    - If you a DRV if you probablitistic behaviour at each point then it is called PMF
  - PDF

- Continous RV
  - A RV which can take all possible value (fraction as well as integral) between certain limit
  - For eg height, weight, age
  - PDF

## Distribution function

- It is also called CDF for all real _x_
- If X is RV then function defined of all real number _x_  by
  - f(X) = P(X <= x) = P {w: X(w) <= x}, -$\infty$ < x < +$\infty$
- Domain of DF is {-$\infty$, +$\infty$} and range of DF is {0,1}

## Remark of distribution function

## Properties of distribution function

- If F is DF of RV X and if _a<b_ , then
  - P(a<X<b) = F(b)-F(a)
- If F is df of RV X , then
  - 0<F(x)<1
