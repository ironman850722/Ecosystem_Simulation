# Ecosystem_Simulation
![image](https://github.com/ironman850722/Ecosystem_Simulation/blob/main/Ecosystem_gorwth.jpg)  

## Introduction
This project mainly uses OpenMP to simulate the ecosystem. The OpenMP here was used to design the code conveniently instead of speedup the code. This is what we called Functional Decomposition. In the above figure, each of the variables will more or less impact other variables, hence, using Functional Decomposition is to assign individual variable to a thread.  

## Variables setup  
The project contains two random factors which are temperature and precipitation. These two factors impact the following variables, which are the height of the grain, the growth of deer, and the number of the beasts. In general, we only need to allocate 3 threads to these 3 variables, however, to make the code simple, I add the fourth variable called "Watcher". This variable, Watcher, doesn't impact those 3 variables, but to print out their monthly value. This Watcher variable, certainly, need a thread to handle it.  

## How to run the code
1. Install linux environment Ex. Ubuntu  
2. In Ubuntu, type "sudo apt update"  
3. Type "sudo apt install build-essential"  
4. Type "gcc --version" to check gcc version  
5. Compile the code " g++ main.c -o main -lm -fopenmp"  
6. Type "./main", and will get all the variables' value in every month.  
