Source code:
https://gitlab.com/0rangFardy/steamstats

This was a web pair project for a distributed systems module, where we were required to create a program with multiple web connections that worked to produce a particular output. In my case, we created a program that retrieved user data from a Steam rankings website, analysed it to give statistics for the users chosen, and outputted it as a pdf. The website we used for this was steamladder.com, which tracks user rankings on various metrics like rank and playtime. This data is freely provided by Steam, though the website was a more convenient middleman that provided data in a json format.

SteamLadder front page:
![image](https://user-images.githubusercontent.com/57454635/156924475-39ceb1b1-0744-414a-86a0-59ea17d83865.png)

Example output of user data (mine):
![image](https://user-images.githubusercontent.com/57454635/156924889-d2bd5ecf-69e6-43ce-aace-6b68d1707915.png)

The analysis was coded by me, which went through the returned jsons and retireved specific pieces of data, then did a bunch of basic statistics calculations on them like average, min and max. The output to the pdf was handled by my partner. Both of these sections ran on a web application made using the Python Flask framework. 

Example output of the overall program:
![image](https://user-images.githubusercontent.com/57454635/156925545-6fc973d5-0365-40ae-aa9d-2af05631f99d.png)

Please note: while this program still compiles it will no longer work. This is because to retrieve Steam data the SteamLadder API required a private authentication key from an existing account. We used a key from my personal account for the program but after it was submitted I revoked the key for privacy reasons, hence it will no longer authenticate.
