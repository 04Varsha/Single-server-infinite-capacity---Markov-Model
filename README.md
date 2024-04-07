# Single server with infinite capacity (M/M/1):(oo/FIFO)
## Aim :
To find (a) average number of materials in the system (b) average number of materials in the conveyor (c) waiting time of each material in the system (d) waiting time of each material in the conveyor, if the arrival  of materials follow poisson process with the mean interval time 12 seconds, serivice time of lathe machine follows exponential distribution with mean serice time 1 second and average service time of robot is 7seconds.

## Software required :
Visual components and Python

## Theory:
Queuing are the most frequently encountered problems in everyday life. For example, queue at a cafeteria, library, bank, etc. Common to all of these cases are the arrivals of objects requiring service and the attendant delays when the service mechanism is busy. Waiting lines cannot be eliminated completely, but suitable techniques can be used to reduce the waiting time of an object in the system. A long waiting line may result in loss of customers to an organization. Waiting time can be reduced by providing additional service facilities, but it may result in an increase in the idle time of the service mechanism.

![image](1.png)

This is a queuing model in which the arrival is Marcovian and departure distribution is also Marcovian,number of server is one and size of the queue is also Marcovian,no.of server is one and size of the queue is infinite and service discipline is 1st come 1st serve(FCFS) and the calling source is also finite.

## Procedure :

![2](https://github.com/04Varsha/Single-server-infinite-capacity---Markov-Model/assets/149035374/5af08c80-12d6-47a2-a366-e160f100d9b6)

## Output :

![OP1](https://github.com/04Varsha/Single-server-infinite-capacity---Markov-Model/assets/149035374/c2d975aa-169b-4538-a8a3-083f523bf12f)

## Experiment:

![292727331-177ee20a-93ef-4557-93af-b65988d549d6](https://github.com/04Varsha/Single-server-infinite-capacity---Markov-Model/assets/149035374/32545f17-5d5d-40e0-8e5f-a17109977e71)


![239145706-1be511c9-fdc1-4532-9973-411dca77f805](https://github.com/04Varsha/Single-server-infinite-capacity---Markov-Model/assets/149035374/d35647c6-823b-41c5-ab2a-58eee63edad7)

## Program

~~~
DEVELOPRD BY : VARSHA A
REGISTER NO  : 212223220121

arr_time=float(input("Enter the mean inter arrival time of objects from Feeder (in secs): "))
ser_time=float(input("Enter the mean  inter service time of Lathe Machine (in secs) :  "))
Robot_time=float(input("Enter the Additional time taken for the Robot (in secs) :  "))
lam=1/arr_time
mu=1/(ser_time+Robot_time)
print("--------------------------------------------------------------")
print("Single Server with Infinite Capacity - (M/M/1):(oo/FIFO)")
print("--------------------------------------------------------------")
print("The mean arrival rate per second : %0.2f "%lam)
print("The mean service rate per second : %0.2f "%mu)
if (lam <  mu):
    Ls=lam/(mu-lam)
    Lq=Ls-lam/mu
    Ws=Ls/lam
    Wq=Lq/lam
    print("Average number of objects in the system : %0.2f "%Ls)
    print("Average number of objects in the conveyor :  %0.2f "%Lq)
    print("Average waiting time of an object in the system : %0.2f secs"%Ws)
    print("Average waiting time of an object in the conveyor : %0.2f secs"%Wq)
    print("Probability that the system is busy : %0.2f "%(lam/mu) )
    print("Probability that the system is empty : %0.2f "%(1-lam/mu) )
else:
    print("Warning! Objects Over flow will happen in the conveyor")
print("---------------------------------------------------------------")
~~~

## Output :

![OP2](https://github.com/04Varsha/Single-server-infinite-capacity---Markov-Model/assets/149035374/7fbba1cf-80d5-4d03-b300-3d4476730d23)

## Result : 
The average number of material in the sysytem and in the conveyor and waiting time are successfully found.

