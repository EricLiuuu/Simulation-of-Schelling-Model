# Simulation of Schelling's Model
Highlights: Data Visualization, Class Inheritance, Model Simulation
## Background
[Schelling's model of segregation](https://en.wikipedia.org/wiki/Schelling%27s_model_of_segregation) is an agent-based model developed by economist [Thomas Schelling](https://en.wikipedia.org/wiki/Thomas_Schelling). His work demonstrates that having people with **"mild"** in-group preference towards their own group could still lead to a highly segregated society [racial segregation](https://en.wikipedia.org/wiki/Racial_segregation).
## Description
In this work, I segmented this problem into several parts and finished the simulation step by step in an easy-to-understand manner. I also conducted a solution for compensating this inevitable trend.

I first created two different groups of agents: "PurpleAgents" and "GoldAgents". They are inherited from the same class: "Agent". 

Let's first test the model with 200 agents of each group. We set the group affinity threshold to 0.51, which means that each purple or gold agent wants to be in a 'block' in which they are in the **majority group**. And here is the result:

<p align="center" width="100%">
    <img width="33%" src="https://github.com/EricLiuuu/Simulation-of-Schelling-Model/blob/main/data/sim1.png">
</p>

Obviously, the segregation is expected. 

Now let's evaluate Schelling's model using 400 agents of each group. We set the group affinity threshold to 0.4, which means that agents do not have a strong preference towards their own group. And here is the result:

<p align="center" width="100%">
    <img width="33%" src="https://github.com/EricLiuuu/Simulation-of-Schelling-Model/blob/main/data/sim2.png">
</p>

From the result, we can see that **even if people don't mind being a minority in their neighborhood, you still get segregation pretty easily according to this model**. For a long time model such as this were used to argue that some degree of segregation was inevitable, and therefore it should not be a target of policy.

How can we fix this issue? We need to introduce some **"diversity seekers"**! In this case, these "diversity seekers" would like to stay in a community in which they are in the **minority group**. I constructed two new classes: "PurpleDiversitySeekers" and "GoldDiversitySeekers". Then I created 300 agents of each group and run the simulation again. Here is the result:

<p align="center" width="100%">
    <img width="33%" src="https://github.com/EricLiuuu/Simulation-of-Schelling-Model/blob/main/data/sim3.png">
</p>

Great, problem solved. But really? This is only a simulation under ideal conditions. People like "diversity seekers" are rare after all. As a result, a diverse community still requires effort from everyone. 

## License

This project is licensed under the MIT License - see the LICENSE.md file for details

## Acknowledgments

* [Bobby Madamanchi](https://www.si.umich.edu/people/bobby-madamanchi)

  Instructional faculty at University of Michigan - Ann Arbor, Department of School of Information
