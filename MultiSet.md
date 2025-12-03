# MultiSet Design

## Introduction

My design is observing a a player inventory built utilizing a Sequence data structure `Sequence<String>`. This sequence data structure will be holding the items and quantity of each item. The inventory within the game will be visualized as a linear (1 dimensional) list of items instead of a grid or other 2 dimensional inventory system. This will allow the sequence data structure to be ideal due to the linear similarities between the structure itself and the inventory setup.

## Design Philosophy

As stated in the introduction, the purpose of utilizing the sequence data structure is because it has a very similar setup as the inventory type used within the game. Since the inventory grows as each unique item is obtained, we only have to expand search time when a unique item is added. Since the inventory is only housing items and item quantities, there should be no reason to over-complicate the data structure by using an AVL tree or other related data structure. We will simply be searching for an item with the same name as the input. There are no uses for having the data structure in sorted order such as using an AVL tree. 

The **user** would be whoever is developing the inventory class. **client** would be the inventory class itself.

## Core Operations



## Set Operations

something

## Extension Feature

something

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

