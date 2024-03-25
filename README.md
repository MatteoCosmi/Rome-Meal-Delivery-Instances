# Meal Delivery Test Instances

This repository contains the instances used in the paper  *"Assigning Orders to Couriers in a Meal Delivery Application via Integer Programming"* by  M. Cosmi, G. Oriolo, V. Piccialli, P. Ventura.

The instance folder contains 33 instances using anonymized data from meal delivery operations at an italian Food Delivery company. 

- Folder **Beta** contains 33 files. Each file provides the average waiting times for the restaurants associated to each order of the instance: $\beta_1$ is the average waiting time of the restaurant associated to order 1.

- Folder **Creation Times** contains 33 files. Each file provides the placement times for each order of the instance. [^1]

- Folder **Targets** contains 33 files. Each file provides the requested delivery times for each order of the instance.

- Folder **D** contains 33 files. Each file provides the distance between pairs of orders (customers delivery locations). Each matrix has the size |O| x |O|, where O is the set of orders

- Folder **D_M** contains 216 files. Each file provides the distance between pairs of couriers and orders (couriers release position and customers delivery locations). Each matrix has the size |C| x |O|, where C is the set of couriers and O is the set of orders

- - Folder **D_bar** contains 216 files. Each file provides the distance between pairs of couriers or orders and orders. Each matrix has the size (|O| + |C|) x |O|, where C is the set of couriers and O is the set of orders

To fully reproduce the experiments performed to produce the results mentioned in the paper, it is necessary to consider a check-out time equal to 1 for all the orders available in the instances. The (complete) distance matrix D_bar, used to build the model, was obtained summing the available D_bar, the check-out time ($alpha$) and the waiting time ($\beta$) at the restaurant: distance(i,j) = d_bar(i,j) + $\beta$(j) + $alpha$(i).

[^1]: Note that in our experiments we rounded these values to multiple of 5.
