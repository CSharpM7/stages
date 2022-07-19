---
layout: page
title: Pictochat
background: grey
---

<div class="col-lg-12 text-center">
	<h2 class="section-heading text-uppercase">Pictochat</h2>
</div>
<img class="img-fluid d-block mx-auto" src="https://ssb.wiki.gallery/images/thumb/0/07/SSBU-PictoChat_2.png/800px-SSBU-PictoChat_2.png" alt="">

### Stencil Animation
It seems that uvSet controls when a vertex gets drawn in. The motion file simply uses Vector31's X coordinate to create the drawing effect. There is also an erasing animation, probably leave the material part of these motion files alone if possible? Not sure how to extend the duration of these animations.

For uvSet, the further the UV coordinate is to the right, the later it gets drawn. Most vertices are to the right of the center.

Some model file changes COULD be dangerous and cause crashes...will research this more.
Numdlb changing is dangerous

### Scene Control
erase_wait controls when the scene ends<br/>
Draw 1st wait SHOULD be for the first scene to start, but also controls every other scene start?!? <br/>
Not sure what draw wait does...apparently nothing? Hmmmm...

Stage scenes are in the order they appear in internal files. SNA: Should not attempt, probably make it another FD.

| Original | Notes | Change | New |
| :---:|:----:|:---:|:---:|
| ![Noses](https://ssb.wiki.gallery/images/thumb/e/e4/Pictochat_2_Jellyfish.jpeg/175px-Pictochat_2_Jellyfish.jpeg)<br/>1| 0x1ae8d0ec87 refers to their wander range | | |
| ![Car](https://ssb.wiki.gallery/images/thumb/8/8b/PictoChat_2_Car.jpg/175px-PictoChat_2_Car.jpg)<br/> 2| Rigged hitbox, road shares model. 0x0e97f09501 could refer to spawns, 0x185e7df818 to something? | | |
| ![25M](https://ssb.wiki.gallery/images/thumb/6/6e/Pictochat_2_Donkey_Kong.jpeg/175px-Pictochat_2_Donkey_Kong.jpeg)<br/> 3| 0x22dfd9ae4b could be barrel spawn time | (Sorry TNN, this gotta go) | |
| ![Pac is Back](https://ssb.wiki.gallery/images/thumb/f/f6/Pictochat_2_PacPix.jpg/175px-Pictochat_2_PacPix.jpg)<br/> 4| 0x18c372196e refers to spawn time and 0x141ed28149 the amount of pacs  | The pac is baaaaaaack | |
| ![PaperPlanes](https://ssb.wiki.gallery/images/thumb/1/1f/PictoChat_2_Paper_Airplanes.jpeg/175px-PictoChat_2_Paper_Airplanes.jpeg)<br/> 5| | | |
| | | |
| | | |
| ![1-2](https://ssb.wiki.gallery/images/thumb/e/ed/PictoChat_2_Girders.jpeg/175px-PictoChat_2_Girders.jpeg)<br/> 6| | Remove center box because of Cave of Life | |
| ![Boots](https://ssb.wiki.gallery/images/thumb/0/06/PictoChat_2_Boots.jpeg/175px-PictoChat_2_Boots.jpeg)<br/> 7| Rigged hitbox and burybox | SNA | |
| ![Poles](https://ssb.wiki.gallery/images/thumb/1/14/PictoChat_2_Poles.jpeg/175px-PictoChat_2_Poles.jpeg)<br/> 8| | Remain the same |![NewPoles](https://ssb.wiki.gallery/images/thumb/1/14/PictoChat_2_Poles.jpeg/175px-PictoChat_2_Poles.jpeg) |
| ![Cloud](https://ssb.wiki.gallery/images/thumb/6/69/PictoChat_2_Clouds.jpeg/175px-PictoChat_2_Clouds.jpeg)<br/> 9| 0x1cf7054041 cloud speed? | | |
| ![Seesaw](https://ssb.wiki.gallery/images/thumb/2/20/PictoChat_2_Seesaw.jpeg/175px-PictoChat_2_Seesaw.jpeg)<br/> 10| | Lowkey keep the same | |
| | | |
| | | |
| ![Sparks](https://ssb.wiki.gallery/images/thumb/f/f0/PictoChat_2_Sparks.jpeg/175px-PictoChat_2_Sparks.jpeg)<br/> 11| Rigged electric hitbox; plats share model | | |
| ![Faucet](https://ssb.wiki.gallery/images/thumb/1/15/Pictochat_2_Faucet.jpg/175px-Pictochat_2_Faucet.jpg)<br/> 12| Conveyor belt + LVD material change? | SNA |
| ![Tornado](https://ssb.wiki.gallery/images/thumb/1/10/PictoChat_2_Tornado.jpeg/175px-PictoChat_2_Tornado.jpeg)<br/> 13| Windbox? 0x164b50cfc7 / 0x1735f08633 correlate to left and right tornado power | | |
| ![Gusty Gus](https://ssb.wiki.gallery/images/thumb/8/82/PictoChat_2_Gusty_Gus_2.jpeg/175px-PictoChat_2_Gusty_Gus_2.jpeg)<br/> 14| Windbox? area_rect_info | | |
| ![Staring Contest](https://ssb.wiki.gallery/images/thumb/9/92/PictoChat_2_Staring_Contest.jpeg/175px-PictoChat_2_Staring_Contest.jpeg)<br/> 15| 0x1f09a6de89? | | |
| | | |
| | | |
| ![Pipes](https://ssb.wiki.gallery/images/thumb/9/90/Pictochat_2_Pipes.jpg/175px-Pictochat_2_Pipes.jpg)<br/> 16| Each pipe has a skeleton attached to it. Could be used for something CRAZY... | Remove warp mechanic, maybe add pipes to the edges of the stage? | |
| ![Road](https://ssb.wiki.gallery/images/thumb/e/e8/PictoChat_2_Road.jpg/175px-PictoChat_2_Road.jpg)<br/> 17| | Remove BG collision | |
| ![Dolphin](https://ssb.wiki.gallery/images/thumb/d/d9/Pictochat_2_Dolphins.jpeg/175px-Pictochat_2_Dolphins.jpeg)<br/> 18| Time delay likely tied to this | | |
| ![Escalator](https://ssb.wiki.gallery/images/thumb/3/34/PictoChat_2_Elevator.jpeg/175px-PictoChat_2_Elevator.jpeg)<br/> 19| Conveyor Belt | SNA | |
| ![Clock](https://ssb.wiki.gallery/images/thumb/4/4e/PictoChat_2_Clock.jpeg/175px-PictoChat_2_Clock.jpeg)<br/> 20| clock controls position of hands. Clock can spawn on the left or right. Might be controlled by bin files, same with rotation. 0x17c9f8dcb6 controls how long this lasts. | Should I bail? Fountain of Dreams? | |
| | | |
| | | |
| ![Sunset](https://ssb.wiki.gallery/images/thumb/4/41/PictoChat_2_Sunset.jpeg/175px-PictoChat_2_Sunset.jpeg)<br/> 21| Unfortunately, both birds share same model. AND THERE'S NO COLLIDER FOR THE SUN?!?!? | | |
| ![Infinity](https://ssb.wiki.gallery/images/thumb/5/5a/PictoChat_2_Infinity.jpeg/175px-PictoChat_2_Infinity.jpeg)<br/> 22| | | |
| ![Pen n Paper](https://ssb.wiki.gallery/images/thumb/6/6a/PictoChat_2_Script.jpeg/175px-PictoChat_2_Script.jpeg)<br/> 23| Writes one line, dabs ink, writes the next line. Lines appear in random? spots disappear eventually. 0x17646e65d2 should refer to this. | | |
| | | |
| 24 is the background for the last 3 | There's no collision on these scenes either | | | | |
| ![Shooting Stars](https://ssb.wiki.gallery/images/thumb/2/27/PictoChat_2_Shooting_Star.jpeg/175px-PictoChat_2_Shooting_Star.jpeg)<br/> 25| | | |
| ![Moon](https://ssb.wiki.gallery/images/thumb/8/86/PictoChat_2_Moon.jpeg/175px-PictoChat_2_Moon.jpeg)<br/> 26| Remove final dark phase | | |
| ![Flashlight](https://ssb.wiki.gallery/images/thumb/b/b3/PictoChat_2_Policeman.jpeg/175px-PictoChat_2_Policeman.jpeg)<br/> 27| | | |