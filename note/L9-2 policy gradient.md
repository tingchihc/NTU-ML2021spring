## YT  
  * https://www.youtube.com/watch?v=US8DFaAZcp4  

## slide  
  * p20-35  

## version 0  
  * Reward delay: actor has to sacrifice immediate reward to gain more long-term reward.  
  * in space invader, only "fire" can yield positive reward.  
  * when RL firstly acts "fire", then RL will always act "fire".  

## version 1  
  * cumulated reward, to make sure, the reward represents which acts.  

## version 2  
  * set a discount factor  
  * Discount factor can make new act has small weight because the previous acts are important.  

## version 3  
  * Good or Bad reward is "relative"  
  * we minus baseline b to make G have positive and negative values.  

## policy gradient  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/pg1.png)  

## on-policy & off-policy  
  * ON-POLICY: The actor to train and the actor for interacting is the same  
  * OFF-POLICY: Can the actor to train and the actor for interacting be different?  

## off-policy -> proximal policy optimization(PPO)  
  * The actor to train has to know its difference from the actor to interact  

## Exploration -> collection training data  
  * The actor needs to have randomness during data collection.  
  * Enlarge output entropy  
  * Add noises onto parameters  

