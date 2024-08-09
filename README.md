Design Report: Implementing Object-Oriented Principles in the Blackjack Game

Object-Oriented Design Choices

1. Encapsulation

Encapsulation is achieved by defining private attributes and providing public methods for accessing and modifying these attributes. The Card class, for instance, encapsulates the value and type of a card and provides methods to access these values.

2. Classes and Objects

Card Class: Represents a single card in the game. It includes attributes for the card's value and type, methods to get the card's numerical value, check if it's an ace, and get the path to the card's image.

BlackJack Class: Manages the game logic and GUI. It includes methods for initializing the game, handling player actions, and updating the game state.

3. Inheritance
In this implementation, inheritance is not used because the game logic and design do not require a hierarchical relationship between classes. The focus is on composition rather than inheritance.

4. Polymorphism
Polymorphism is not explicitly used in this basic implementation. However, the use of interfaces or abstract classes could be introduced if the game were expanded to include different types of card games or players.

Implementation Details
Card Class
Attributes: value and type.
Methods:
toString(): Returns the string representation of the card.
getValue(): Returns the card's numerical value, with special handling for face cards and aces.
isAce(): Checks if the card is an ace.
getImagePath(): Returns the file path for the card's image.
BlackJack Class
Attributes:

deck: List of cards in the deck.
random: Random object for shuffling the deck.
dealerHand, playerHand: Lists to hold the cards for the dealer and player.
dealerSum, playerSum: Sums of the card values for the dealer and player.
dealerAceCount, playerAceCount: Counts of aces in the dealer's and player's hands.
frame, gamePanel, buttonPanel, hitButton, stayButton: GUI components.
Methods:

BlackJack(): Constructor to initialize the game and GUI.
startGame(): Starts a new game by building and shuffling the deck, and dealing initial cards.
buildDeck(): Builds the deck of cards.
shuffleDeck(): Shuffles the deck.
reducePlayerAce(), reduceDealerAce(): Adjusts the sum of card values if there are aces and the sum exceeds 21.
Event Handling:

hitButton and stayButton have action listeners to handle player actions and update the game state accordingly.
The paintComponent method in gamePanel is overridden to handle custom drawing of the cards and game messages.
Graphical User Interface
The GUI is built using Java Swing components. The JFrame is the main window, and it contains two panels:

gamePanel: Displays the cards and game messages.
buttonPanel: Contains the "Hit" and "Stay" buttons.
The paintComponent method in gamePanel handles the drawing of the cards and the game result messages.

Instructions to Compile and Run the Game

Prerequisites
Ensure you have the Java Development Kit (JDK) installed on your system.

Steps to Compile and Run
Save the Code: Save the provided code in a file named BlackJack.java.

Compile the Code:
Open a terminal or command prompt and navigate to the directory where BlackJack.java is saved. Run the following command to compile the code:

javac BlackJack.java

Run the Game:
After successful compilation, run the game using the following command:

java BlackJack

Gameplay:

The game window will open with a green background representing the game table.
The player's cards will be displayed at the bottom, and the dealer's cards at the top.
The "Hit" and "Stay" buttons allow the player to draw a new card or hold their current hand, respectively.
The game result will be displayed in the middle of the window after the player chooses to "Stay".