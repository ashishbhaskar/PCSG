Path Choice Set Generation Algorithms
This repository contains various code files implementing different algorithms aimed at solving the path choice set generation problem. In this context, path choice set generation refers to the process of determining a set of feasible routes between origin-destination pairs in a transportation network.
Each algorithm in this project relies on a shortest path finding algorithm, and for this purpose, we have employed Dijkstra's algorithm. Dijkstra's algorithm efficiently computes the shortest path between two nodes in a graph, which serves as a fundamental building block for our path choice set generation methods. Python is the primary programming language used for coding these algorithms. Its simplicity, versatility, and rich libraries make it an ideal choice for implementing the intricate algorithms involved in this project. Furthermore, we have developed and tested these algorithms in the Jupyter Notebook environment. Jupyter Notebook allows for interactive computing and code visualization, making it easier to comprehend and modify the code for different use cases.
In this README file, you will find information about each algorithm, its purpose, and instructions on how to run and use them. Additionally, we have provided sample datasets and usage examples to help you get started quickly. We encourage you to explore and experiment with these algorithms to find the most suitable path choice set generation method for your specific requirements.
If you have any questions or suggestions, feel free to reach out to us.
Setup
There are two forms of setup required to successfully run the scripts:
I.	Environment Setup
II.	Input datasets
For environment setup, you should have python language and the Jupyter notebook setup. Dependencies and external libraries are detailed in the file called “Requirements.txt” which can be installed using the following command:
pip install -r Requirements.txt
Input datasets are in the form of shapefiles. The files are available in the folder named “datasets”. Simply providing the required hyperparameters for each algorithm is sufficient to run the algorithm successfully. The hyperparameters for each algorithm are detailed below in their respective sections. Each algorithm takes one common input in the form of origin and destination ID. Each algorithm begins with generating the graph structure in the form of a nested dictionary with weights given by the specified column, such as “Total_Kilo” for distance as weights. 
Link Elimination
This algorithm only requires one input in the form of number of paths required. This can be given using the attribute labelled as ‘k’, short-hand for k-shortest path problem. The algorithm by default generates one path if k is not specified. 
Link Labelling
Link labelling algorithm can be run using the same script as link elimination. The setup requires the number of paths generated to be defaulted to one path and the weights of the graph can be changed by simply changing the column used to generate the graph. The output is a list containing the paths for specified origin and destination pair.
Simulation technique
Simulation method requires the following inputs:
I.	Distribution 
II.	Number of draws
These parameters can be adjusted in the section labelled as “Input parameters”. The output is a list containing the paths for specified origin and destination pair.
Branch and Bound 
Branch and bound technique requires four input parameters. These parameters can be provided in the form of either a tuple or a list. The order of these values are as follows:
1.	Distance constraint
2.	Temporal constraint
3.	Loop constraint
4.	Similarity constraint
The method also requires a bounding parameter to limit the radius of search which is specified by the variable “bounding_factor” in the section labelled as “Input parameters”. The output is a list containing the paths for specified origin and destination pair.
Probabilistic Approach
This method requires minimal inputs. The most significant setup is to generate a set of paths to limit the search area which can be done using any of the above-mentioned algorithms. Within the script provided, we have used link elimination method with 20 paths. This can be updated according to the desired input of the analyst. 
