# Intro to neural network and backpropogation

- micrograd is a auto gradiation system used to do backpropogation
- derivative 
  - f'(x) = lim (h -> 0) [f(x + h) - f(x)] / h 
  - how the function's output (y) changes with respect to a small change in the input (x) at that particular point.


- derivative on multiplying function
  - L =  a * b
  - dL/da = (f(x+h) - f(x))/h = ((a+h)*b -(a*b))/h = (a*b + h*b -a*b)/h = b
  - similarly dL/db = a
- derivative on addition function
  - L = a + b
  - dL/da = (a+h+b) - (a+b)/h = (a+h+b-a-b)/h = h/h = 1
  - dL/db =1

- chain rule is import in backprop
  - dz/dx = dz/dy . dy/dx
- tanh -> squash funtion

- topological sort
  - Left to right ordering of a DAG
  - in order to apply backward all the computations need to be executed
  - ie: all the nodes before the end nodes should be computed

- 1:55:54 doubt

- learning rate decay: reduces learning rate after each epochs
- Always do zero grad before back prop or you will end up adding the previous gradient values
