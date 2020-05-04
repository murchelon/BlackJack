# BlackJack
 
# BlackJack 0.3
# =============
#
# Blackjack game created to help me learn python.
# The goal is make a program that can play by it's own
# and show the statistics envolved. Expanded to be an real, rich, fast and reliable
# player strategy test ambient
#
# Features:
# =========
#
# - Algoritm that trys to mimic reality the best it cans. The goal is to use ALL rules in BJ and try to create a fast and real envirolment to try differente alooritms to beat the dealer
# - Can use several players with and a dealer
# - hability to use real decks with cards and suits
# - able to use different algoritms to decide if hit ot not
# - Can use as many decks as desired in a given match
# - The decks are consumed by each match and when its near exaustion, the dealer get new decks
# - can look to the cards in the dealer (player "sees" dealer hand)
# - Possible to run hundred of tousands of simulations
# - Multiprocessing, Multithreading (give a number of simulations to a process and create several processes)
# - Set the precision of calculus used and in results
#
# T O D O List:
# =============
#
# - TODO: Implement insurance, the amout payied for insurance, the amout payed by blackjack .. all in parameters
# - DONE -- Fix the order of the dealed cards. They have an order... and it must be followed
# - TODO: make this program be able to play against flash sites with bj games
# - DONE -- Implement spliting of cards
# - DONE -- Implement betting
# - DONE -- Implement push (tie, when neither the player or dealer wins. Today when there is a tie, the dealer wins)
# - DONE -- Implement double
# - DONE -- Implement surrender
# - TODO: Implement algorigm of Machine Learning (this is the main original goal)
# - TODO: Implement algoritm of Card Counting (Hi-Lo ? Must me able to do 2 types of CC: One like the real world and other with simulated real decks "in mind")
# - DONE -- Implement Multithreading to compare performance. Probably worse
# - DONE -- Implement Multiprocessing by NOT using a Pool .. to compare performance
# - TODO: export lots os data and shit to use with Jupyter and Plot and Numpy and etc
# - TODO: Implement game against a human (1 and 2 players ?)
# - TODO: Create a GUI ?
# - DONE -- Find a way to show progress when in multiprocessing mode
# - DONE -- Support more then 1 player (computer dealer x computer x computer...)
# - DONE -- Implement some way of measuring the speed, like 2323 matches / sec
# - DONE -- Implement a real behavior for the dealer. Follow bj rules for dealer
# - TODO: Change several aspects of the program to make it faster. like using sets and many other little changes
# - TODO: Stop using lists ! use NumPY for everything! Performance!
# - TODO: Implement pays more when blackjack (natural)
# - TODO: Add SEVERAL small rules that can be found in https://en.wikipedia.org/wiki/Blackjack
#
#
# - FIX: --  There are sometimes when i try to pop a card from the current deck, but
#            as there are so many players (in games with >30 players) that there is no card to pop
#            need to implement a wat to detect there is no card and create a new current deck. Probably have to make current deck a global var
#
# - FIX: -- When i use 3 players with 1 match... the statistics look wrong. Have to check that
#
# RULES and DETAILS:
# ==================
#
# - Dealer must hit if lower then 16. If ctHIT_ON_SOFT_HAND = True then see comment in the variable
# - Order of play: Dealer gives a card for each player, one for him face up. Then one again for each player and one for him again
# - If using more them one player, the results of them are combined averaged
# - If using more them one task, the results of them are combined averaged
# - The number of decks may be increased in order to accomodade the number of players
# - If the remaining cards in the deck are only ctRESHUFFLE_DECK_PERC (in percentual), then get new shuffled decks up tho the amount of decks defined in the param
# - If player blows, the dealer wins even before he plays (make a huge difference, giving more advantage to the dealer)
# - Can only split once, having 2 game at once
# - Can only split if the FIRST 2 cards are equal. First hand
#
#
# References:
#
# https://pdfs.semanticscholar.org/e1dd/06616e2d18179da7a3643cb3faab95222c8b.pdf
# https://www.888casino.com/blog/blackjack-strategy-guide
# https://www.888casino.com/blog/advantage-play/an-introduction-to-advanced-advantage-play
# https://www.888casino.com/blog/blackjack-tips/why-not-mimic-the-dealer-playing-strategy