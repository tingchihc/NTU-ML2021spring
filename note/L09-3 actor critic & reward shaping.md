## yt  
  * https://www.youtube.com/watch?v=kk6DqWreLeU  
  * https://www.youtube.com/watch?v=73YyF1gmIus  

## Actor-critic  
  * Critic: Given actor 𝜃, how good it is when observing 𝑠 (and taking action 𝑎)  
  * Value function 𝑉𝜃(𝑠) : When using actor 𝜃, the discounted cumulated reward expects to be obtained after seeing s  
  * The output values of a critic depend on the actor evaluated.  

## Estimate 𝑉𝜃(𝑠)  
## Monte-Carlo(MC) based approach  
  * The critic watches actor 𝜃 to interact with the environment.  
  * After seeing 𝑠𝑎, Until the end of the episode, the cumulated reward is 𝐺𝑎′  
  * After seeing 𝑠𝑏, Until the end of the episode, the cumulated reward is 𝐺b'  

## Temporal-difference(TD) approach  
  * {St,at,rt,St+1}...  
  * 𝑉𝜃(𝑠𝑡) = 𝑟𝑡 + 𝛾𝑟𝑡+1 + 𝛾2𝑟𝑡+2 …  
  * 𝑉𝜃(𝑠𝑡+1) = 𝑟𝑡+1 + 𝛾𝑟𝑡+2 …  
  * 𝑉𝜃(𝑠𝑡+1) = 𝛾𝑉𝜃(𝑠𝑡)+rt  

![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/version3.5.png)  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/version4.png)  
![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/tipofactor-critic.png)  

## Reward shaping -> The developers define extra rewards to guide agents  
  * If 𝑟𝑡 = 0 in most cases -> We don’t know actions are good or bad.  
