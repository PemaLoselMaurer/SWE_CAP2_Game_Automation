# Programming the Farming Drone (Report)

## Introduction
"The Farmer Was Replaced" is a Python coding game that challenges players to automate farm management tasks. In this game,
we use Python code to take over the duties of a fictional farmer who has been automated out of his job. Our goal is to
write scripts that manage essential farming activities—such as planting, watering, harvesting, and trading crops—while
maximizing profits and efficiently managing resources. Each level introduces new challenges, requiring us to apply
programming concepts like loops, conditionals, functions, and data management to solve problems effectively. 
This educational game combines coding skills with strategic thinking, making it both fun and informative.

# Table of Contents
- [Code Snippets and Explanation](#code-snippets-and-explanation)
- [Challenges and Learnings](#challenges-and-learnings)
- [References](#references)

## vidio's link
- https://drive.google.com/drive/folders/1UFD6OWnz6CPz-XzQtxSMOxpQhOU_BYsM?usp=sharing

## Step 1: Farming on 1 tile
  *Demo:*
    Video Demo:
    ![](./step_1.mp4)
  *Code:*
  1.harvest()

  2.while True:
        harvest()
   
  *Explanation:*
   - First we need to harvest about 5 hays manually to unlock the loop so the code can run infinite number of times and
    harvest the grass with the if condition.
  *Notes*
   - With the code above i collect enough hay to unlock speed and grass to be able to go to next tile
   - Features unlocked : loop

## Step 2: Farming on 1x3 tile
  *Demo:*
    Video Demo:
    ![](./step_2.mp4)
  *Code:*
  while True:
       plant(Entites.Bush)
       move(South)
       do_a_flip()
       harvest()
   
  *Explanation:*
   -By unlock plant and expand, the tile then becomes from 1 to 3, then after unlocking plant we use the above code
    which will repeatedly plant bushes and move south in the field, does a flip and then it will harvest the crops and the bushes.
  *Notes*
   - Using the code above I collect enough hay and wood to unlock the senses and operator
   - Features unlocked : operators

## Step 3: Farming on 3x3 tile
  *Demo:*
    Video Demo:
    ![](./step_3.mp4)
  *Code:*
  while True:
      for i in range(get_world_size()):
          for j in range(get_world_size()):
              move(South)
              plant(Entities.Bush)
          move(East)
          do_a_flip()
      for i in range(get_world_size()):
          for j in range(get_world_size()):
              move(South)
              harvest()
          move(East)

  *Explanation:*
   - The code makes the farmer Move through the field grid, planting bushes in every grid box.After planting the entire grid, it goes
     back to harvest from each planted bush. The process repeated endlessly because of the while True loop.
  *Notes*
   - Using the code above I collect enough hay and wood to unlock carrots
   - Features unlocked : carrots

## Step 4: Farming carrots on 3x3 tile
  *Demo:*
    Video Demo:
    ![](./step_4.mp4)
  *Code:*
(f1)
  trade(Items.Carrots_seed)

(till)
  while True:
      for i in range(get_world_size()):
          for j in range(get_world_size()):
              move(East)
              till()
          move(North)
    
(main)
   while True:
      for i in range(get_world_size()):
          for j in range(get_world_size()):
              plant(Entites.Bush)
              move(East)
          move(North)
          do_a_flip()
      for i in range(get_world_size()):
          for j in range(get_world_size()):
              harvest()
              move(East)
          move(North)

  *Explanation:*
   - The code makes the farmer first tarde the wood for carrot seeds. then it moves through the field grid, planting carrot seed in every grid box.
     After planting the entire grid, the carrots grows and it goes back to harvest from each planted carrots.
    The process repeated endlessly because of the while True loop.
  *Notes*
   - Using the code above I collect enough hay , wood, and carrots to unlock tree, sunflowers, pumkins, multi trade, 4x4 tile, and watering.
   - Features unlocked : Functions and varibles

## Step 5: Farming carrots on 4x4 tile
  *Demo:*
    Video Demo:
    ![](./step_5.mp4)
  *Code:*
(f1)
  trade(Items.Empty_Tank)

(till)
  while True:
      for i in range(get_world_size()):
          for j in range(get_world_size()):
              move(East)
              till()
          move(North)
    
(main)
   while True:
      for i in range(get_world_size()):
          for j in range(get_world_size()):
              use_item(Items.Water_Tank)
              plant(Entites.Bush)
              move(East)
          move(North)
          do_a_flip()
      for i in range(get_world_size()):
          for j in range(get_world_size()):
              harvest()
              move(East)
          move(North)

  *Explanation:*
   - The code makes the farmer first tarde the wood for carrot seeds. then it moves through the field grid, planting trees in every grid box
     and watering them as the farmer drone moves. After planting the entire grid, the grows grows and the the drone waits for the tree to grow
     until it goes back to harvest from each planted carrots.
     The process repeated endlessly because of the while True loop.
  *Notes*
   - Using the code above I collect enough wood to upgrade most of the resourses which are upgradeable.
   - Features unlocked : Functions and varibles

# Challenges and Learnings
   ## Challenges
    The challenges are writing algorithms that are both efficient and effective,Small errors could cause the entire farming operation to malfunction.
    new coding concepts,the code can get long and hard to read and planting depends on available resources, harvesting depends on growth stages
   ## Learnings
    Automation Skills: Practice breaking down processes into logical steps and implementing the code.
    Control Flow Mastery: Gain experience with loops and conditionals for task management.
    Object-Oriented Concepts: Manage states with variables and objects.
    API Use: Understand how to interact with and implement external libraries.

## References
1. [Youtube](https://www.youtube.com/)
2. [wiki.gg](https://thefarmerwasreplaced.wiki.gg)
