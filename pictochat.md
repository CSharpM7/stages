---
layout: page
title: Pictochat
background: grey
---

<div class="col-lg-12 text-center">
	<h2 class="section-heading text-uppercase">Pictochat</h2>
</div>
<img class="img-fluid d-block mx-auto" src="https://ssb.wiki.gallery/images/thumb/0/07/SSBU-PictoChat_2.png/800px-SSBU-PictoChat_2.png" alt="">

# Note to future pictochat modders
For the brave souls attempting to mod this stage: improper edits of numshb and numdlb files WILL cause your stage not to load. To avoid crashes:
- Make sure the meshes' names are the same as the source name (if you want a custom planeA mesh, make sure it is named `bone_005planeAShape` )
- When exporting via carlos tools, don't forget to reassign the bones to the mesh in studioSB/ssbh_e! Meshes won't appear if they aren't assigned the proper bone
- I recommend not removing meshes, but instead either grey them out (use an HSV of 0,0,0.259993 for vertex colors) and put them somewhat behind the stage (z of -35) to still show that a current scene is active

### Stencil Animation
It seems that some combination of map1 and uvSet controls when a vertex gets drawn in. The motion file uses Vector31's X coordinate to create the drawing effect44. There is also an erasing animation, probably leave the material part of these motion files alone if possible? Not sure how to extend the duration of these animations.

For map1, the further the UV coordinate is to the right, the later it gets drawn.


### Scene Control
erase_wait controls when the scene ends<br/>
Draw 1st is the wait range for the first rotation <br/>
The last draw is the wait range after the first cycle finishes. By cycle, I mean 20 scenes have been played, it resets. Ya it's...kinda weird...

Stage scenes are in the order they appear in internal files. SNA: Should not attempt, probably make it another FD.

### TODO:
- [ ] SFX
- [ ] UI
- [ ] Disable Stars
- [ ] Disable Flashlight?
- [ ] Randall over Gusty Gus
- [ ] Car Scene
- [ ] Sparks Scene
- [ ] Pipes
- [ ] Figure out Sunset Collision
- [ ] Staring Contest?
- [ ] Disable Clock
- [ ] Disable Pac Attack

| # | Original | Notes | Change | New |
| :-: |:---:|:----:|:---:|:---:|
|1 | ![Noses](https://ssb.wiki.gallery/images/thumb/e/e4/Pictochat_2_Jellyfish.jpeg/175px-Pictochat_2_Jellyfish.jpeg)| `0x1ae8d0ec87` refers to their wander range | Platforms that move up and down and wander around | |
|2 | ![Car](https://ssb.wiki.gallery/images/thumb/8/8b/PictoChat_2_Car.jpg/175px-PictoChat_2_Car.jpg)| `0x0e97f09501` could refer to spawns, `0x185e7df818` to something? | | |
|3 | ![25M](https://ssb.wiki.gallery/images/thumb/6/6e/Pictochat_2_Donkey_Kong.jpeg/175px-Pictochat_2_Donkey_Kong.jpeg)| `0x22dfd9ae4b` could be barrel spawn time,  `0x134ab3b224` cam pos | (Sorry TNN, this gotta go) Warioware! | <img src="assets/img/pictochat/dk.png" alt="newdk" width="175"/> |
|4 | ![Pac is Back](https://ssb.wiki.gallery/images/thumb/f/f6/Pictochat_2_PacPix.jpg/175px-Pictochat_2_PacPix.jpg)| `0x141ed28149` the speed of pac1 , `0x1422dfbe10` speed of other pacs. 0x17329e7064 onward deal with pac coordinates. 0x170ffe59d4 is x 0x141ed28149 is y  | Hardcoded collision, cant do anything with this| |
|5 | ![PaperPlanes](https://ssb.wiki.gallery/images/thumb/1/1f/PictoChat_2_Paper_Airplanes.jpeg/175px-PictoChat_2_Paper_Airplanes.jpeg)| Plane spawn order is randomized| Fountain of Dreams (except middle platform also rises) | <img src="assets/img/pictochat/plane.png" alt="newlift" width="175"/> |
| | | | |
| | | | |
|6 | ![1-2](https://ssb.wiki.gallery/images/thumb/e/ed/PictoChat_2_Girders.jpeg/175px-PictoChat_2_Girders.jpeg)| | Remove center box because of Cave of Life | <img src="assets/img/pictochat/lift.png" alt="newlift" width="175"/> |
|7 | ![Boots](https://ssb.wiki.gallery/images/thumb/0/06/PictoChat_2_Boots.jpeg/175px-PictoChat_2_Boots.jpeg)| Rigged hitbox and burybox. Motion handled internally? | hitboxes removed, not sure what to do with this | |
|8 | ![Poles](https://ssb.wiki.gallery/images/thumb/1/14/PictoChat_2_Poles.jpeg/175px-PictoChat_2_Poles.jpeg)| `0x1b54f707a7 / 0x1a00b4c840` frame plats descend | Remain the same |![NewPoles](https://ssb.wiki.gallery/images/thumb/1/14/PictoChat_2_Poles.jpeg/175px-PictoChat_2_Poles.jpeg) |
|9 | ![Cloud](https://ssb.wiki.gallery/images/thumb/6/69/PictoChat_2_Clouds.jpeg/175px-PictoChat_2_Clouds.jpeg)| `0x1880339f33-0x18c216984e` cloud speed | If we can move the cloud position that'd be nice | |
|10 | ![Seesaw](https://ssb.wiki.gallery/images/thumb/2/20/PictoChat_2_Seesaw.jpeg/175px-PictoChat_2_Seesaw.jpeg)| | Lowkey keep the same | ![NewSeesaw](https://ssb.wiki.gallery/images/thumb/2/20/PictoChat_2_Seesaw.jpeg/175px-PictoChat_2_Seesaw.jpeg) |
| | | | |
| | | | |
|11 | ![Sparks](https://ssb.wiki.gallery/images/thumb/f/f0/PictoChat_2_Sparks.jpeg/175px-PictoChat_2_Sparks.jpeg)| `0x0d16ab9468` determines boundaries. Rigged electric hitbox; plats share model | PM Green Hill? | |
|12 | ![Faucet](https://ssb.wiki.gallery/images/thumb/1/15/Pictochat_2_Faucet.jpg/175px-Pictochat_2_Faucet.jpg)| Conveyor belt + LVD material change? | SNA | ![NewFaucet](https://ssb.wiki.gallery/images/thumb/1/15/Pictochat_2_Faucet.jpg/175px-Pictochat_2_Faucet.jpg) |
|13 | ![Tornado](https://ssb.wiki.gallery/images/thumb/1/10/PictoChat_2_Tornado.jpeg/175px-PictoChat_2_Tornado.jpeg)| Windbox? `0x164b50cfc7 / 0x1735f08633` correlate to left and right tornado power | Tornado greyed and inactive | |
|14 | ![Gusty Gus](https://ssb.wiki.gallery/images/thumb/8/82/PictoChat_2_Gusty_Gus_2.jpeg/175px-PictoChat_2_Gusty_Gus_2.jpeg)| Windbox? `area_rect_info` | Randall? | |
|15 | ![Staring Contest](https://ssb.wiki.gallery/images/thumb/9/92/PictoChat_2_Staring_Contest.jpeg/175px-PictoChat_2_Staring_Contest.jpeg)| `0x1f09a6de89`? | Oh man wtf | |
| | | | |
| | | | |
|16 | ![Pipes](https://ssb.wiki.gallery/images/thumb/9/90/Pictochat_2_Pipes.jpg/175px-Pictochat_2_Pipes.jpg)| Each pipe has a skeleton attached to it. Could be used for something CRAZY... | Remove warp mechanic, make Town and City | |
|17 | ![Road](https://ssb.wiki.gallery/images/thumb/e/e8/PictoChat_2_Road.jpg/175px-PictoChat_2_Road.jpg)| | Remove BG collision | ![NewRoad](https://ssb.wiki.gallery/images/thumb/e/e8/PictoChat_2_Road.jpg/175px-PictoChat_2_Road.jpg) |
|18 | ![Dolphin](https://ssb.wiki.gallery/images/thumb/d/d9/Pictochat_2_Dolphins.jpeg/175px-Pictochat_2_Dolphins.jpeg)| Time delay likely tied to this. Position controlled via animation | Platforms come into the stage randomly | |
|19 | ![Escalator](https://ssb.wiki.gallery/images/thumb/3/34/PictoChat_2_Elevator.jpeg/175px-PictoChat_2_Elevator.jpeg)| Conveyor Belt | BF | |
|20 | ![Clock](https://ssb.wiki.gallery/images/thumb/4/4e/PictoChat_2_Clock.jpeg/175px-PictoChat_2_Clock.jpeg)| clock controls position of hands. Clock can spawn on the left or right. Might be controlled by bin files, same with rotation. `0x17c9f8dcb6` controls how long this lasts. `0x19b99af1fd` speed of drawing? | If we could only control where this spawns... | |
| | | | |
| | | | |
|21 | ![Sunset](https://ssb.wiki.gallery/images/thumb/4/41/PictoChat_2_Sunset.jpeg/175px-PictoChat_2_Sunset.jpeg)| THERE'S NO COLLIDER IN THE LVD FILE FOR THE SUN?!?!? | | |
|22 | ![Infinity](https://ssb.wiki.gallery/images/thumb/5/5a/PictoChat_2_Infinity.jpeg/175px-PictoChat_2_Infinity.jpeg)| Chooses a random set of platforms to be active | Walls | <img src="assets/img/pictochat/infinity.png" alt="newinfinity" width="175"/> |
|23 | ![Pen n Paper](https://ssb.wiki.gallery/images/thumb/6/6a/PictoChat_2_Script.jpeg/175px-PictoChat_2_Script.jpeg)| Writes one line, dabs ink, writes the next line. Lines appear in random? spots disappear eventually. `0x17646e65d2` should refer to this. | |![NewPen](https://ssb.wiki.gallery/images/thumb/6/6a/PictoChat_2_Script.jpeg/175px-PictoChat_2_Script.jpeg) |
| | | | |
|24 | background for the last 3 | There's no collision on these scenes either | This scene can also load on its own without any of the next 3 gimmicks | | | | |
|25 | ![Shooting Stars](https://ssb.wiki.gallery/images/thumb/2/27/PictoChat_2_Shooting_Star.jpeg/175px-PictoChat_2_Shooting_Star.jpeg)| `0x1518a1ffbc` | | | |
|26 | ![Moon](https://ssb.wiki.gallery/images/thumb/8/86/PictoChat_2_Moon.jpeg/175px-PictoChat_2_Moon.jpeg)| `0x186ce6a6ec` scene length. `0x1f0bc8f27d` has some influence on blackout effect |Remove final dark phase | |
|27 | ![Flashlight](https://ssb.wiki.gallery/images/thumb/b/b3/PictoChat_2_Policeman.jpeg/175px-PictoChat_2_Policeman.jpeg)| | | | |