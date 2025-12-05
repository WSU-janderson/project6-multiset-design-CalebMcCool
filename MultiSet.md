# MultiSet Design

## Introduction

My design is observing a a player inventory built utilizing a Sequence data structure `Sequence<String>`. This sequence data structure will be holding the items and quantity of each item. The inventory within the game will be visualized as a linear (1 dimensional) list of items instead of a grid or other 2 dimensional inventory system. This will allow the sequence data structure to be ideal due to the linear similarities between the structure itself and the inventory setup.

## Design Philosophy

As stated in the introduction, the purpose of utilizing the sequence data structure is because it has a very similar setup as the inventory type used within the game. Since the inventory grows as each unique item is obtained, we only have to expand search time when a unique item is added. Since the inventory is only housing items and item quantities, there should be no reason to over-complicate the data structure by using an AVL tree or other related data structure. We will simply be searching for an item with the same name as the input. There are no uses for having the data structure in sorted order such as using an AVL tree. 

The **user** would be whoever is developing the inventory class. **client** would be the inventory class itself.

## Core Operations

Core operations when utilizing the sequence data structure would be remove, pop, contains, and clear. When looking into the remove operation, this would be utilized if a player trades an item or sells an item. The operation would remove the item from the players inventory as well as remove the quantity (if the player trades or sells all of that item). The time complexity of the remove operation would be O(n) because the linked list could possibly be searched in its entirety before reaching the correct item. 

The **pop** operation would be good for removing the latest item gained by the player. This would be useful if the player goes over a trap or some type of negative interaction, and is punished by having the latest aquired item be stripped from them. The time complexity of the pop operation would be O(1) because it does not need to search the list, it just needs to pop the item on the top of the list. 

The **contains** operation would be useful for a lot of cases in a video game, for this example we can look at a door which needs a key to pass. If the key is in the players inventory, the player can pass, and if the player does not contain the key, they cannot pass. The contains operation would have a time complexity of O(n) because at it's worst case, the entire list may need to be traversed. 

The **clear** operation is good for when a player dies or gets robbed. If the player dies, the entire inventory's data structure can be deleted and a new inventory or sequence data structure is initialized. The time complexity of this operation would be O(1) because all it's doing is erasing the data structure and initalizing a new one. 

The **remove** data structure would be good for either dropping an item, or buying an item from a shop. If the player has currency on them, the remove operation can remove the amount of currency the player is holding based on the price of the item. The time complexity of this would be O(n) because the currency could be anywhere within the players inventory. 

## Set Operations

When looking into the `difference_with()` operation, we can see the items you have but another player does not have. This is particularly useful when entering a common area with other live players and bartering specific items which another player has that you don't. This can be in the context of a trading house or some other common area for players. This operation will look at each item in your inventory and compare it to each item in the other players inventory, if the other player does not have the item, that item is flagged and the operation continues out until it has checked every item. After the operation checks every item, a menu is displayed showing all the items you do not have that the other player has. The other player views the same menu but its items you have that they currently don't have. 

This operation will not explicitly manipulate the sequence data structure, but it will view it multiple times and perform it's own operations based on the data it sees. The conceptual time complexity of this would be O(n) because it will have to check every item in your inventory as well as every item in the other players inventory. 

## Extension Feature

The new capability for my multi-set would be `craftRecipe()`. This feature would be perfect to implement on a player's inventory because it can check to see if you have all the correct items needed to craft the recipe. It can also utilize the remove function to remove those items based on the quantity of items needed within the recipe. This could save syntax and possibly runtime if you incorporated the craftRecipe() function with the inventory's sequence data structure. Everything would be closely tied together and could perform at good speeds because of the minimal code additions needed to implement this craftRecipe() function. 

## UML Diagram / Abstraction Boundary

something

## Trade-off Analysis

something

## Alternative Design Sketch

something

## Evaluation Plan

something

## Conclusion / Reflection

something

