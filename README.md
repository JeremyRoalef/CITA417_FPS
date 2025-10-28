<h1>Overview</h1>
This lab aims to develop a system for enemy wave spawning and completion. In doing so, I reinforced my understanding of Unreal's object-component system and learned how to create custom data structures. The end results of the lab is a rudimentary enemy wave spawner with a system in place to check for wave completion. Here's how the setup works:
1) The world is filled with spawn points that enemies may spawn at. Each spawn point has a flag for whether enemies may spawn at the position or not. In this setup, this flag was not utilized.
2) The world contains a singular enemy spawn manager. This holds the logic for spawning in enemies, the delay between enemies spanwing, and the delay between waves spawning. This acts as a middleman between the spawn points in the world and the enemy being instantiated into the world.
3) Enemies spawning. When an enemy spawns, they have a health component, movement logic, and an attack behavior.

<h1>Blueprints</h1>
<ol>BP_SpawnPoint</ol>
<img width="437" height="164" alt="image" src="https://github.com/user-attachments/assets/c471f18c-d316-4435-8240-d8f7412aba79" />


<ol>BP_WaveManager</ol>
<img width="1020" height="220" alt="image" src="https://github.com/user-attachments/assets/98f8a091-3bc8-43dc-9b6f-bdc879955389" />

<h1>Video</h1>
![2025-10-10 12-35-11](https://github.com/user-attachments/assets/db96ad22-1b12-4285-979b-bd81ee99a299)


<h1>Analysis</h1>
Making a wave spawner is simple. Create a spawn point system, a manager for wave spawning, the enemy spawning behavior, and create some enemy variants. While working on this lab, one problem was evident: visual scripting is very restrictive. Visual scripting may be a great tool for beginnners with low-complexity code. However, creating a wave manager highlighted how hard it is to control the pin flow in a logical and visual manner. In the BP_WaveManager above, you may see some pin connections traversing across the entire system with minimal control over how they get there. This could be reduced completely with text-based programming.

In short, visual scripting is not ideal for mid-high complexity programming. In the future, I will look to converting my project into C++ scripting.
