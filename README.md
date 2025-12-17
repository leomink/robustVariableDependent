
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

## Replicating
The src folder contains all the source code in Java with the implementation of all the optimization models described in the manuscript and the instance generators for all the experiments. 

To run the code and fully replicate the experiments, you will need to make sure that you have a valid license for <code>CPLEX</code>. The project contains four packages named "RobustCSP", "RobustDD", "RobustSensitivityExp", and "RobustVD". Package "RobustCSP" contains all the source code related to the constrained shortest path featured application. The package "RobustDD" contains all the code related to the DD reformulation approach. The package "RobustVD" contains all the code related to the cutting-plane approach, and the package "RobustSensitivityExp" contains all the code for the miscelaneous sensitivy experiments reported in the paper.   

For Eclipse users, the "RobustVarDependent.zip" file provides an Eclipse project ready to be imported. 


## Dataset 
The problem instances generator is included in package "RobustVD". Class "Datahandler" contains a method "genRandomInstance" to generate the synthetic instances. When creating a "Datahandler", the required inputs are the number of variables, the number of uncertain parameters, the number of leader constraints, and the number of constraints defining the uncertainty set. For the method "genRandomInstance", the inputs are a seed for the random number generator and a righ-hand side multiplier to control to tightness of the constraints. The method "outputInstance" exports an instance into the mps/aux format required for MiBS using the single-follower formulation. 

For the featured application, the original networks are in the "data" folder in DIMACS format. Each line stores the tail of an arc, the head of an arc, its cost, and its resource consumption. The class "Datahandler" in the package "RobustCSP" has a method to read the problem instance in DIMACS format and a "genRandomInstance" method that randomly generates the values of the arc weigths.  
