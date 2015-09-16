# getting-started
Demo repository to get familiar with using Github


#Amelia was here. 
\No new line at the end of file

#Amelia Guise_Assignment 1
#(My answers are off- my players seem to have made exponentially more money that in the official answers- which is good for them and bad for me). 

import random

gameStake = 50  
cards = range(10)

#Defining the class Players

class Player:
    PlayerID = 0
    Pot= 0   
    LastCard=0

#use two input variables to initialise the ID and starting pot of each player

    def __init__(self, inputID, startingPot):
        self.playerID = inputID
        self.pot = startingPot
        
   #Create a code for selecting a random card. 
             
    def play(self,dealerCard):
        playerCard = random.choice(cards)
        
    #Conditional: tests the player's card value against the dealer card.
    #defines whether the player has won or lost.
    #tallies up the players pot. 

        
        if playerCard < dealerCard:
            self.pot-=gameStake
            return 'Lose,' + str(playerCard) + 'vs' + str(dealerCard)
        else:
            self.pot-=gameStake
            return 'Win' + str(playerCard) + 'vs' + str(dealerCard)
    
    #create an accessor function to return the current value of the player's pot

    def returnPot(self):
        return self.pot
        
    #create an accessor function to return the player's ID
    def returnID(self):
        return self.playerID
        
# Next we will create some functions outside the class definition which will control the flow of the game
# The first function will play one round. It will take as an input the collection of players, and iterate through each one,
# calling each player's '.play() function

def playHand(players):
    
        for player in players:
            print player.play(random.choice(cards))

def checkBalances(players):
    
    for player in players:
        print 'player ' + str(player.returnID()) + ' has $' + str(player.returnPot()) + ' right.'
        
gameStake=500
cards = range(10)

players = []      

for i in range(5):
    players.append(Player(i, 500))
    
    for i in range(10):
        print ''
        print 'start game ' + str(i)
        playHand(players)
    
print ''
print 'game results:'
checkBalances(players)


%run "/Users/ameliaguise/Documents/SEMESTER TWO/DATA MINING THE CITY/AJG Assignment 1.py"

start game 0
Lose,5vs8

start game 1
Lose,2vs7

start game 2
Win7vs7

start game 3
Win8vs1

start game 4
Lose,0vs5

start game 5
Win3vs0

start game 6
Lose,4vs9

start game 7
Win7vs1

start game 8
Win7vs3

start game 9
Lose,1vs2

start game 0
Win6vs4
Lose,6vs9

start game 1
Win5vs2
Lose,5vs9

start game 2
Lose,2vs3
Lose,0vs6

start game 3
Win7vs3
Lose,4vs6

start game 4
Lose,1vs8
Lose,3vs6

start game 5
Win7vs4
Win4vs3

start game 6
Win2vs2
Lose,0vs4

start game 7
Win7vs5
Lose,3vs7

start game 8
Win6vs3
Lose,0vs2

start game 9
Win2vs1
Win9vs2

start game 0
Win6vs1
Win6vs0
Lose,2vs6

start game 1
Lose,0vs2
Lose,1vs9
Lose,0vs3

start game 2
Win4vs2
Lose,8vs9
Lose,4vs8

start game 3
Lose,3vs5
Win2vs2
Win6vs5

start game 4
Win9vs5
Lose,1vs2
Win9vs9

start game 5
Lose,0vs4
Win4vs0
Lose,6vs7

start game 6
Lose,5vs6
Lose,0vs3
Win6vs1

start game 7
Lose,2vs4
Win4vs1
Win7vs6

start game 8
Win5vs3
Lose,7vs9
Win4vs0

start game 9
Win3vs2
Win6vs5
Lose,4vs6

start game 0
Lose,2vs6
Win5vs4
Win8vs6
Win8vs4

start game 1
Lose,1vs6
Win9vs1
Lose,4vs9
Win5vs2

start game 2
Win7vs1
Win9vs1
Win4vs2
Win8vs1

start game 3
Win3vs2
Lose,3vs7
Win7vs2
Lose,1vs3

start game 4
Lose,2vs7
Win9vs4
Lose,3vs4
Lose,3vs6

start game 5
Win8vs2
Win2vs2
Lose,3vs5
Lose,4vs7

start game 6
Lose,4vs9
Lose,5vs9
Lose,1vs5
Win2vs2

start game 7
Win7vs1
Lose,6vs7
Win6vs4
Win5vs2

start game 8
Win9vs2
Win9vs5
Win5vs0
Win9vs1

start game 9
Win6vs4
Lose,4vs7
Lose,3vs6
Win9vs7

start game 0
Lose,3vs7
Win4vs4
Win3vs0
Win1vs0
Lose,3vs8

start game 1
Lose,2vs5
Lose,6vs9
Lose,1vs6
Win8vs1
Lose,0vs6

start game 2
Lose,0vs5
Win7vs0
Win6vs6
Lose,3vs8
Win6vs2

start game 3
Lose,1vs9
Lose,3vs9
Win8vs3
Win9vs4
Win4vs2

start game 4
Win9vs1
Win2vs0
Lose,5vs8
Lose,4vs9
Win6vs6

start game 5
Win9vs3
Lose,1vs8
Win1vs0
Win0vs0
Lose,6vs8

start game 6
Win9vs4
Win3vs3
Lose,1vs3
Lose,3vs5
Win7vs1

start game 7
Lose,1vs2
Lose,2vs7
Lose,6vs9
Lose,1vs9
Lose,7vs9

start game 8
Win8vs7
Lose,0vs1
Lose,2vs3
Lose,2vs6
Win7vs7

start game 9
Win9vs0
Win4vs4
Win5vs1
Win3vs1
Win7vs0

game results:
player 0 has $-24500 right.
player 1 has $-19500 right.
player 2 has $-14500 right.
player 3 has $-9500 right.
player 4 has $-4500 right.


