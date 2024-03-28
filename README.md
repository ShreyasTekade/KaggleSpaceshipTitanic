This is my solution to Kaggle's "Spaceship titanic" competition.

Notes:
Year: 2912
We've received a transmission from four lightyears away
The Spaceship Titanic was an interstellar passenger liner launched a month ago. With almost 13,000 passengers on board, the vessel set out on its maiden voyage transporting emigrants from our solar system to three newly habitable exoplanets orbiting nearby stars.
you are challenged to predict which passengers were transported by the anomaly using records recovered from the spaceship’s damaged computer system.

Evaluation Metric:
Submissions are evaluated based on their classification accuracy, the percentage of predicted labels that are correct.

Submission Format:
The submission format for the competition is a csv file with the following format:

PassengerId,Transported
0013_01,False
0018_01,False
0019_01,False
0021_01,False
etc.

Data Dictionary:
Personal records for about two-thirds (~8700) of the passengers, to be used as training data.
PassengerId - A unique Id for each passenger. Each Id takes the form gggg_pp where gggg indicates a group the passenger is travelling with and pp is their number within the group. People in a group are often family members, but not always.
HomePlanet - The planet the passenger departed from, typically their planet of permanent residence.
CryoSleep - Indicates whether the passenger elected to be put into suspended animation for the duration of the voyage. Passengers in cryosleep are confined to their cabins.
Cabin - The cabin number where the passenger is staying. Takes the form deck/num/side, where side can be either P for Port or S for Starboard.
Destination - The planet the passenger will be debarking to.
Age - The age of the passenger.
VIP - Whether the passenger has paid for special VIP service during the voyage.
RoomService, FoodCourt, ShoppingMall, Spa, VRDeck - Amount the passenger has billed at each of the Spaceship Titanic's many luxury amenities.
Name - The first and last names of the passenger.
Transported - Whether the passenger was transported to another dimension. This is the target, the column you are trying to predict.

1: Import Data
2: Feature Engineering
    - Created additional variables: Passenger Group, Split of Cabin as Cabin1, Cabin2 & Cabin3, Total AMount Spent, Group Size, Family Size
3: MIssing Value Treatment
4: EDA