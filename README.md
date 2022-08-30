# solve-a-simple-maze-problem-by-the-Dyna-Q-algorithm
this repository contains python code of the simple maze problem on page 165 of [Sutton and Andrew's RL book](http://incompleteideas.net/book/RLbook2020.pdf). I've created this repository for educational purposes, you can use, change or modify it.
## what is Dyna-Q
Dayna-Q is combination of model-base and model-free RL.<br >
I want to explaine model-free, model-based and Dyna-Q algorithms by a simple example you can read chapter 8 of [Sutton and Andrew's RL book](http://incompleteideas.net/book/RLbook2020.pdf) for more mathematical and detailed informations.
- model-based RL
<img src='https://user-images.githubusercontent.com/74808396/187433829-413896bd-29bd-4721-acd4-e147f81480ac.png' width='300' heigth='400'>
for understanding model-based RL, imagine you are watching the simple above grid world from above. you can see what will happen if you take each action, what reward you will get, and what is the next position that you will get into that. so you start planning, take action in your mind, and observe reward. you measure the value of each position by the goal position in other words you say to yourself going to this position how much will help me for reaching the goal position?. according to your knowledge you start acting in the grid world and calculate the value of each position in the world, so after enough experience, you will know the value of all positions and you can simply go in the position that has the highest value.   

- model-free RL
<img src='https://user-images.githubusercontent.com/74808396/187442288-b4de0626-36b7-494a-a9dd-32671a41e71d.png' width='300' heigth='400'>

you can understand model-free RL with above image. you are in the **white** spot, all world is ambiguous for. you can just take action and observe reward and next state. for each action that you have taken in the world you estimate the value of that state action pair and update your estimation with respect to given reward and value of next state . value of each state action pair calculated with respect to its contribution to reach us to the goal spot .

- Dyna-Q

<img src ='https://user-images.githubusercontent.com/74808396/187447185-5edae91e-0f65-4af2-a424-15a40e1b35dc.png' width='300' heigth='400'>

Dyna-Q is a combination of model-free and model-based algorithms. you can understand it with the above image. like model-free RL at the beginning the world is ambiguous for you. you start gathering data and updating initila estimation of the value of the state action pair but as you update your value expectation, you remember the dynamic of the observed sections of the world so after enough data you know some part of the world so beside taking action and gathering data in the world you can do planning in white spots and update your estimation like model-based algorithm.

## environment 

we use the simple maze environment introduced on page 165 of [Sutton and Andrew's RL book](http://incompleteideas.net/book/RLbook2020.pdf). I've implemented all necessary codes in `Tabular Dyna-Q` notebook.

## how to run code

- just run the `Tabular Dyna-Q` notebook.
- have fun :wink:
