### Invasive Weed Optimization

##### Reference: Mehrabian A R, Lucas C. A novel numerical optimization algorithm inspired from weed colonization[J]. Ecological Informatics, 2006, 1(4): 355-366.

| Variables | Meaning                                           |
| --------- | ------------------------------------------------- |
| ipop      | The initial population size                       |
| mpop      | The maximum population size                       |
| iter      | The maximum number of iterations                  |
| smin      | The minimum number of seeds                       |
| smax      | The maximum number of seeds                       |
| isigma    | The initial value of standard deviation           |
| fsigma    | The final value of standard deviation             |
| lb        | The lower bound (list)                            |
| ub        | The upper bound (list)                            |
| pos       | The position of seeds (list)                      |
| score     | The score of seeds (list)                         |
| dim       | Dimension                                         |
| gbest     | The score of the global best agent                |
| iter_best | The global best score of each iteration (list)    |
| con_iter  | The last iteration number when "gbest" is updated |

#### Test problem

$$
f(x)=\sum_{i=1}^{30}x_i^2,\qquad -10\leq x_i\leq10, \quad
i=1,\cdots, 30.
$$


#### Example

```python
if __name__ == '__main__':
    ipop = 20
    mpop = 100
    iter = 2000
    smin = 0
    smax = 5
    isigma = 1
    fsigma = 1e-6
    lb = [-10] * 30
    ub = [10] * 30
    print(main(ipop, mpop, iter, smin, smax, isigma, fsigma, lb, ub))
```

##### Output:

![convergence curve](C:\Users\dell\Desktop\研究生\个人算法主页\Gravitational Search Algorithm\convergence curve.jpg)

The IWO converges at its 2000-th iteration, and the global best value is 1.4811243161587636e-06.

```python
{
    'best score': 1.4811243161587636e-06, 
    'best solution': [0.0004018456981121767, -3.2682599447569955e-06, -9.455509392674457e-05, 5.188477312079762e-05, 0.00017137500067564303, -0.00012223522965487042, 0.00011623617641158009, -0.000124118982871797, 4.8569097120283375e-05, 0.0002976310355268008, 6.15705239072025e-05, 8.077446302055623e-05, 0.00020276163906065369, -0.0002811285829622663, -0.0003058244802800531, -0.00018882593646512292, -0.00031291318574091793, -7.098423681308358e-05, -0.000472572417336426, 0.00011401801538079769, 0.0002072860452717333, 0.00016774266470804766, 0.00016678967570886395, -0.00011968615297976984, -0.00038220692876286274, 0.00023839458936768734, -0.00026706592368278285, -0.0002001935540331373, -0.00033141460343734765, 8.664523587924919e-05], 
    'convergence iteration': 2000
}
```

