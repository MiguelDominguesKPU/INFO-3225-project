# INFO-3225-project
top-down tile-based dungeon-crawler game with randomly generated levels.

Implemented in Processing: A java-based API and IDE for streamlined graphics rendering and input processing.

Implemented skills:

- Very modular, extendable and encapsulated design.
- Practiced OOP principles such as encapsulation, inheritence, polymorphism/dynamic binding, data-hiding, and abstraction.
- Randomly-generated maps that are built recursively and represented as an n-ary tree.

Design Patterns practiced:

- State: - to seperate the multiple game states (start, running, end) and handle user input.
- Factory-Builder: - Encapsulates game object and game level creation into a simple set of methods.

Overview of application flow:

1. Program uses States to determine input/output and where user is at in the application. Game state changes are done within state classes via method calls.

2. When the user starts the game, the RunningGameState class contains most of the main game loop code. Factory builder classes will initilize the rooms and the game objects (items, enemies) in those rooms. A level contains data on all it's own rooms. All of the game objects (rooms, enemies) encapsulate it's own data and interact with other classes via methods.

3. As user moves in the game, MovingObjectController and CollisionDetector classes contain game logic for how player character and game objects interact. The Actionable and Combatable interfaces define how game objects interact with other objects.

4. When a user finds the exit to a level, a new level is randomly built or the game ends.
