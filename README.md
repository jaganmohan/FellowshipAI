# FellowshipAI
Models for Fellowship.AI program

The recommender model has been implemented based on the paper 
Collaborative Recurrent Neural Networks for Dynamic Recommender Systems, Young-Jun Ko, Lucas Maystre, Matthias Grossglauser, ACML, 2016.

The model has been implemented with:
  - Artist IDs as the only input </br>
  W<sub>h</sub> * h(t-1) + W<sub>aid</sub> * aid 
  - Artist IDs and Tags as input </br>
  W<sub>h</sub> * h(t-1) + W<sub>aid</sub> * aid + W<sub>tag</sub> * tag

for GRU cell  
