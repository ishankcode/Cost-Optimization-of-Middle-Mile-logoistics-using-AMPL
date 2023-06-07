# Cost-Optimization-of-Middle-Mile-logoistics-using-AMPL

### <ins>TOOLS</ins>
Used Ampl and both CPLEX as well as GUROBI Solver. <br />
1. File with following name _mod.txt is the model file.
2. File with following name _dat.txt is the data file.
---

### <ins>Project</ins>
The middle mile delivery stage of the supply chain is when products are moved between facilities before being picked up for delivery. A middle-mile delivery often takes a path from a holding or fulfillment center to a distribution hub.

![image](https://github.com/ishankcode/Cost-Optimization-of-Middle-Mile-logoistics-using-AMPL/assets/66678343/32637a2a-d48e-4e6c-989a-6fbbcbb4b7b7)

<ins>Problem Statement:</ins>
Oops ("Fictitious Company") targets the luxury market. While its prices are higher, it guarantees that products/packages will be delivered on or before a given deadline (measured in hours) or the product is free. Oops wants to optimize its Middle Mile Logistics by reducing the cost incurred in the Middle Mile. The total cost incurred in Middle Mile Logistics for Oops is made up of the operating cost of vehicles, relocation cost of operators, and the cost of the package if delivered late.
There are certain parameters and operating constraints given by Oops to ISEN consulting firm which have to be taken into account while developing the Mixed Integer Linear Programming model: </br>
1.Package : Origin Shipping Center, Destinantion, Weight, Delivery time limit, cost, Package Incompatibilities
2. Vehicle: 3 types of vehicles - with weaight capacity of each vechile type, number of vehicles available.
3. Operators: Every operator trained to handle each vehcile, limited number at each facility, In case of high demand can be relocated at extra cost.
4. Trip: Operational cost per mile for each vehicle, No overloading allowed
5. Center: Cannot exceed the max loading/unloading of vehicles at each center.

<ins>Assumptions</ins>
- The allocation of vehicles from the depot to shipping centers is instantaneous at the beginning of the day.
- The relocation of operators from their home shipping centers to other shipping centers is instantaneous at the beginning of the day.
- Each vehicle starts at one shipping center and goes directly to the destination shipping center. That is, vehicles will not make intermediate loading/unloading stops.
- The loading and unloading of vehicles happen instantaneously.
- The distance between shipping centers is the same irrespective of the vehicle type (as the distance between point A to point B may be different when traveling via road, rail or plane).


Developed a mixed integer linear programming model with 18 parameters, 4 Decision Variables, and 15+ constraints (operator’s availability, product incompatibility, type & number of vehicles, loading/unloading capacity at centers, etc) to optimize the middle mile logistics. <br />

### <ins>Check the report for complete Explanations of the Parameters, Decision Variables, all contraints with Mathematical Explanation and how the constraint was created.</ins>

2 Phases of the project: <br />

i) Developing the MILP Model based on various conditions/ rules set by the company. some of them are 
 described below : 
   - Package Incompatibilities - packages of certain types are incompatible and must be delivered in 
 separate vehicles.
   - Operators - As per the model each facility has a fixed number of operators, but based on demand - 
 operators can be relocated. 
   - Maximum weight capacity of the vehicle.
   - Limits on loading/unloading of vehicles at each facility.

ii) Use the developed model to solve based on the data provided and recommend the best-optimized 
 plan based on the analysis of the result. <br />

As part of recommendations also Conducted multiple sensitivity analyses (What-if questions) on the model for Computational efficiency (Decreased the computation time by 16.5%), Route Incompatibility, and Cost analysis based on additional restrictions that will help in better decision-making for the client.
