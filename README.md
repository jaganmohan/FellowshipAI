# FellowshipAI
Models for Fellowship.AI program

# Problem
Recommending 'K' songs at any time 't' to a user by looking at the past history of user from 1 to time 't-1', where time step implies the event of listening to an artist.

Trying to recommend by modelling the conditional probability during training which tries to model the personalized taste of an user and collaborative effect of other users tastes,
    <b> P(y<sub>t</sub>|1..y<sub>t-1</sub>) </b>
where, y<sub>t</sub> is the next artist user listens to.

During testing the model I recommend 'K' songs to the user, here I validate by checking how good the model was able to predict the next artist user by using K = 1 over testing data and measuring the efficiency.

The recommender model has been implemented based on the paper 
Collaborative Recurrent Neural Networks for Dynamic Recommender Systems, Young-Jun Ko, Lucas Maystre, Matthias Grossglauser, ACML, 2016.

The model has been implemented with:
  - Artist IDs as the only input </br>
  W<sub>hu</sub> * h(t-1) + W<sub>aid</sub> * aid </br>
  - Artist IDs and Tags as input </br>
  W<sub>hu</sub> * h(t-1) + W<sub>aid</sub> * aid + W<sub>tag</sub> * tag

<p><b>W<sub>hu</sub></b> tries to capture personalized taste of an user and</br>
<b>W<sub>aid</sub></b> tries to capture the collaborative effect from all users</br></p>
for GRU cell  
<br/>
<p>Optimizer: RMSProp <br/>
Loss objective: cross entropy
</p>
