# CG Proto 2 Power Guide

## Soldering the Batteries

I don’t really have any authority to speak on whether or not you should solder batteries, but I’ve heard that generally it’s not a good idea, but you _can_ do it. In my experience, it works. This is my method. It’s probably not the best, but it works.

To get familiar with the concept of applying molten metal to bombs that explode really slowly, I watched this video: [https://www.youtube.com/watch?v=Zx7d5yJdWp0](https://www.youtube.com/watch?v=Zx7d5yJdWp0)

You must ensure that you have cells that you _can _solder to (such as these: [https://www.18650batterystore.com/products/samsung-35e](https://www.18650batterystore.com/products/samsung-35e)).

Wrap your batteries in **fish paper**. This is a very insulating material, and will form a good rigid “body” for your battery. The kind I use has adhesive on one side, which makes assembly very easy.

<p align="center">
<img src="/guides/images/power/fish_paper.jpg" height="300">
</p>

Then, with a screwdriver, scrape the anode of the battery. This will remove oxidation and make solder stick much more easily. _Immediately_ afterwards, get a blob of solder on there with your iron. I set mine to 410 degrees Celsius. The reason you want it so hot is because you wanna spend as little time soldering the cell as possible. Speed is the name of the game here. Get your solder on there quick, and get your iron out of there quicker. **Do not hold your iron to the cell for longer than 5 seconds. **At best, it will degrade your battery, and at worst, you’ll have some cool burns.

<p align="center">
<img src="/guides/images/power/blobs.jpg" height="300">
</p>

We’ve got three blobs on there: Two for connecting the batteries, one for the wire going to the BMS.

_Note: You should try to solder the edges, rather than the center, as that will be less likely to cause damage to the cell. Instead of doing what I did, you should probably remove some of the pink shielding and solder to the side of the cell, as that is negatively charged._

Next, cut a wire to connect the batteries. I use copper, solid core, 22AWG. Put it across the battery as shown below. I find that it helps to secure it in place with tape.

<p align="center" float="left">
<img src="/guides/images/power/unsoldered_negative_wire.jpg" height="300">

<img src="/guides/images/power/taped_cells.jpg" height="300">
</p>

Once again, scrape oxidation off the solder blob, grab your rosin core solder, then get your iron on there **_quick_**. Five seconds max should do it. Use extra solder to get things to liquify and adhere.

<p align="center">
<img src="/guides/images/power/negative_wire.jpg" height="300">
</p>

Nice. Once you’re done with that, flip the battery to the cathode. You’re gonna do the same thing, with one key difference: Since we’re soldering cells in parallel, we want the BMS positive wire to be on the opposite cell from the BMS negative wire. For example, if you’re looking at your battery from one side, and you soldered the extra blob on the negative side onto the left cell, you’ll want the extra blob on the positive side to be on the right cell. This will help ensure that current moves through both cells relatively evenly.

<p align="center">
<img src="/guides/images/power/positive_wire.jpg" height="300">
</p>

Now, it’s time to attach the BMS. First, solder two wires of generous length to the extra solder blobs. These will connect to the BMS. I used electrical tape to hold them down while I solder them. **It is extremely important that you do not let these wires touch. You will get cool-looking electrical burns.**

<p align="center" float="left">
<img src="/guides/images/power/positive_bomb.jpg" height="300">
<img src="/guides/images/power/defusing_the_bomb.jpg" height="300">
</p>
Cut the XT30 _really_ short. There should be almost no cable jutting out from the pack. We won’t need it.

<p align="center">
<img src="/guides/images/power/ready_to_tape.jpg" height="300">
</p>

That’s basically it. I like to secure the connector in place with some electrical tape, then wrap the whole thing in a layer or two of kapton tape.

<p align="center">
<img src="/guides/images/power/finished_battery.jpg" height="300">
</p>
