Sorry for the text wall, my Github skillz don't exist, I'm working on formatting this

---

Designing Starlight has been a rollercoaster of an experience. Below I'll go through the process of designing it, why I made some of the design decisions I did, and go on tangents about some minute detail.

---

Let me preface this by saying that many of the mechanisms and concepts in Starlight are found in the [Voron](https://vorondesign.com/) 2.4 and Trident printers, as I have to get ideas somewhere lol. I did **not**, however, reuse any parts, as 1- they don't fit due to me using 8020's 2020 extrusions, and not Misumi's, and 2- If I'm going use concepts from another project (which I already don't like, but again, gotta get ideas SOMEHOW), I don't want to outright steal the parts involved, so I spent the many tedious hours redesigning parts again, and again, and again (looking at you, XY joints, rev. 3.6). 

# Z-Drive gearboxes-
  Why are they so [boxy](https://c7.alamy.com/comp/RDFKHT/cat-sitting-in-a-small-cardboard-box-and-looking-towards-camera-RDFKHT.jpg), you may ask. And the answer is this: My design skills kinda sucked ass at this point, after the basic frame shape (and only the lower part of that), the gearboxes were the first thing I designed. If I were to redesign them, I'd probably do something different. For example, the middle section # **[DON'T FORGET TO INSERT IMAGE. ALSO WHILE YOU'R AT IT, MAKE EXPLODED VERSIONS OF ALL SUBASSEMBLIES]** <- if you're reading this when it goes public, and it has a message about exploded subassembly views; someone tell me.  moving on; the middle section (hopefully pictured above) is unfortunately designed in a way that needs supports. Thankfully,  I was able to design it that the side which needs supports is flat, and dimensions non-critical. It's the only part that needs supports, as I designed Starlight to be as supportless as possible. 

 ---
### Note- You know what, I'll go not in a logical order, but in the order that I designed stuff, as well as logical, to make it extra non-logical (spoiler alert- I put off a lot of important stuff "for later", so some stuff will appear later)
---

# Frame
I wanted something unique for the frame, and the idea of a DIY belt-driven [Prusa XL](https://www.prusa3d.com/en/product/original-prusa-xl-assembled-single-toolhead-3d-printer/)-esque design appealed to me. Hence the reason of the lack of front extrusions, and the... situation that is housing the z-drive gearboxes. 

**[insert exploded frame here]** 

It's turned out quite well, especially given how much I played with dimensions while working. For example (tangent time), while on XY joint revision 2.1, I realized that I didn't have anywhere near enough space. (of course, i had just under 20mm to work with, per XY joint, I had to add another 20mm to the width, making the interior extrusion-to-extrusion width go from 390mm to 400. (tangent over)

My personal favorite part of the frame is the electronics enclosure. Given the that is a more standard Core-XY design than a 2.4, more Trident-like, just minus the three lead screws, and some positioning changes, the space behind the bed was completely useless. The space was just used by the X-axis and the 30mm+ between back of the extrusion and center of the nozzle, as well as the drive units. That was some 60-70 **check actual dimension** mm wasted space, and adding the full thickness of an electronics backpack just seemed stupid. So, instead the entire space underneath the rear of the X-axis and drive units was converted to electronics bay space.

**[insert side profile here]**

It also gives it a more interesting side profile, as shown above, and lowers the depth of the printer, and the ratio of how far forward the bed is to how much space is behind, which I personally find very important. (in case you haven't noticed by now, many decisions made were for aesthetic reasons, because of course they were.) 

The one downside I can currently find is that the DIN rails (which all the expensive electronics and power supplies are mounted to) are mounted directly to the 3mm acrylc, with no other mounting available. (the sheer amound of space needed to cram in a 2020 extrusion and step-adaptor so my panels stay flush isn't viable, for now). I'll update this once Starlight is built and tested.

---

# Bed/Z-axis

I'll turn this one into a double, because they go hand-in-hand anyways. In case you didn't already know, Starlight uses a run-of-the-mill 300mm Voron 2.4 bed. Why? Because they're relatively cheap, and I don't have to design/make it myself, and they're already easy to work with.

Starting with the Z-axis portion of this, Starlight runs quad linear rails- 2 on each side, spaced some 60mm apart. In between the two rails is a 9mm GT2 belt, spaced more towards the rear rail. (*Why use a 2 sided, belt driven approach?*, you ask. And to that, I say, check the section on the frame. The Prusa XL styling makes the front corner movement a non-option (told you aesthetics defined some major decisions), and i felt that having rear movement would be uneccesary.)

The belt driven portion is due to my overblown and phobia-like fear of Z-wobble. I don't care what or why it won't affect me, I'm going with belt driven. Looks better, and allows for faster Z travel.
