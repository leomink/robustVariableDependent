
<img width="1143" height="306" alt="mp" src="https://github.com/user-attachments/assets/0247218e-1fd4-4dfb-8ebc-72892c0dae2b" />

# On solving integer robust optimization problems with integer decision-dependent uncertainty sets
This archive is distributed under the [MIT License](LICENSE).

The purpose of this repository is to share the codes, instances, and results used in the paper ["On solving integer robust optimization problems with integer decision-dependent uncertainty sets"](https://rdcu.be/euoVi), authored by Leonardo Lozano and Juan Borrero.

## Cite
To cite the contents of this repository, please cite the paper as:
```
@article{discreteRobust,
  title={On solving integer robust optimization problems with integer decision-dependent uncertainty sets: L. Lozano, JS Borrero},
  author={Lozano, Leonardo and Borrero, Juan S},
  journal={Mathematical Programming},
  pages={1--33},
  year={2025},
  publisher={Springer}
} 
```

## Dataset 
The "data" folder contains all the datasets used in the paper, including the shortest path networks in DIMACS format and the project selection (knapsack) problem instances. For the project selection problem instances, the files display the nominal profits, the weigths, and the right-hand-side coefficient. The name of the files present the size (network size for shortest path and number of items for knapsack) as well as the random seed used for its generation (a number between 0 and 9 corresponding to each one of the ten replicas per configuration).   

## Replicating
The src folder contains all the source code in Java with the implementation of all the optimization models described in the manuscript. 

To run the code and fully replicate the experiments, you will need to make sure that you have a valid license for <code>CPLEX</code>. The project contains two packages named "KP" and "SP". Package "KP" contains all the source code related to project selection problems modeled as knapsack problems while package "SP" contains all the source code related to the shorstest path problems. 

For Eclipse users, the "combinatorialProbing.zip" file provides an Eclipse project ready to be imported. 
