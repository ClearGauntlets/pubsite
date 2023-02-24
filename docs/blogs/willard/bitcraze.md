# Creating a More Accessible Tracker Using the Bitcraze Lighthouse Positioning Deck
### 2023-02-24

## Introduction
When I began working on ClearGauntlets last year, it quickly became apparent that tracking was gonna be a bear of a project. For some reason, I figured that it was a solved problem. Somebody _must_ have created a simple, easy-to-build device on the cheap to talk to Valve's cool lighthouses. And I was _very_ wrong. This post will explain what I wanted to do, how wrong I was about how easy it would be to do so, and what my plan is going forward.

**TL;DR: I've purchased a Bitcraze Lighthouse Positioning Deck and want to make my own Lighthouse 2.0 trackers because I am curious to see if I can.**

## The Problem
VR tracking is, actually, an insanely complicated challenge. One that took AAA engineers decades to figure out and create a consumer product that didn't _quite_ cost $1000. During the later half of the 2010's, hackers gained some traction on reverse engineering Valve/HTC's Lighthouse tech. From those efforts came [libsurvive](https://github.com/cntools/libsurvive), an effort to fully unravel the stack, from the protocols that the lighthouses use to communicate with tracked devices, to the solving equations embedded in Valve's proprietary blobs. It's a truly incredible project that has been a huge inspiration to me on my short VR journey so far.

However, these guys are focused on how to take Valve hardware and make it talk to their software. What I needed for the ClearGauntlets project was basically the opposite: Taking our hardware and getting it to talk to Valve software. ClearGauntlets is supposed to be a "More Premium™" Haptic Glove solution. Our target kit price is $200, all included. We're a fork of the LucidVR project, whose Prototype 4.1 glove is supposed to cost somewhere around $60. However, they don't include in that price things like the batteries and trackers. That project relies on you either finding a way to mount your controller to your hand, or dropping a few hundred on something like Vive Trackers. I didn't like that, so I wanted to find a way to incorporate tracking into our gloves.

## Research

We didn't have a lot of options. Because I only had an original, 2016-vintage HTC Vive, knew very little about VR, and yet was somehow the resident expert on the team, I decided to target the SteamVR ecosystem. I figured that it would be easy enough, and we went about googling. In a few weeks, we had only found two "open source" solutions for DIY tracked devices: The [HiveTracker](https://hivetracker.github.io/), and the [Vive DIY Position Sensor](https://github.com/ashtuchkin/vive-diy-position-sensor). These looked like great options, until we realized that they were 7-ish years old. Not only that, but they only supported Lighthouse 1.0, and not the newer Lighthouse 2.0.

Until we found these projects, I didn't really grasp the fact that there _were_ two versions of Lighthouse tracking, _and_ that if Lighthouse 1.0 was a Cessna prop plane, Lighthouse 2.0 was an F-18. 2.0 brought a slew of improvements and optimizations to SteamVR infrared tracking, and explaining the details and multitude of complications therein is out of scope here. What's important is that I very quickly realized that 2.0 tracking was _not_ a solved problem for hackers, this entire problem is the kind of thing that people write about for their PhD thesis, and if someone was going to do it, it would be difficult and expensive.

So we focused on Lighthouse 1.0 for now. It wasn't what we wanted, but we figured it would be good enough for the better-than-proof-of-concept gloves that we were trying to make. Lots of people—myself included—still had Lighthouse 1.0 gear, right?

That was in October-ish. I kept reading. Eventually, sometime around December, I found the [Bitcraze Lighthouse Positioning Deck](https://www.bitcraze.io/products/lighthouse-positioning-deck/), a board sold by Bitcraze designed to enable their open-source drone platform to be tracked with Lighthouse 2.0 technology. This was.... what I was looking for. All their source code, schematics, documentation, _everything_ is available on their website for free. The board even has solder points for serial connections. I thought, "What the hell!? How come someone hasn't hacked this thing already?" I asked around on the LucidVR Discord, and the primary reasons, of course, are cost, and engineering effort. This board is $90, plus tax, plus shipping, comes out to $120. For that, you could get a Vive tracker that's plug-and-play, no fuss. It doesn't make sense for your average hacker to buy a "development" board for the price of a market-ready product when they are trying to make a pair of haptic gloves or whatever.

The whole time I was researching, I had been made aware through a friend of mine the SteamVR HDK. Essentially, back in the mid 2010's, Valve had created a suite of hardware devices and software tools to help people make SteamVR compatible tracked devices. This would be perfect for this project, if only they still sold them. I've had a pretty tough time tracking down info, but to my understanding, the project is pretty much dead, unfortunately. A lot of [links on their page are dead or broken](https://triadsemi.com/steamvr-tracking/). There is still a lot of info on the software on Steam's website and other places.

Another project worth mentioning is [Tundra Labs' SIP](https://tundra-labs.com/products/tl448k6d-vr-system-in-package-for-steamvr-tracking?variant=39421399859409), but that has also been out of stock for months. Their datasheets do offer some nice inspiration.

## A Long Road Ahead

I, however, am stupid. A fool, you might say. I hadn't yet realized that VR is actually _pretty expensive_. I wasn't ready to accept that my "all-included" gloves probably needed an extra $100 tacked on _at least_ for an off-the-shelf tracking solution. However, I also realized that in order to take all of Bitcraze's IP and turn it from a drone product _back_ into a SteamVR product would take a lot of time, effort, and money. So, I let the idea sit for a while.

Until today. Today, my Bitcraze Lighthouse Positioning Deck arrived in the mail, all $120 of it. If you're on the `#tracking-solutions` channel on the LucidVR Discord, you'll probably have seen me raving about this project. I've decided that I need to take a step. I'm not really in this to _play VR games._ I'm in this because the tech is cool as hell. I've got this board, and I'm going to see if I can talk to it. Then, I'm going to see if I can program it. Then, I'm going to see if I can hack it. I'll be documenting my progress on this website. Probably on this page, so check back for regular updates.

## The Plan

<img src="/media/bitcraze-in-hand.jpg" style="display: block; margin: 0 auto"/>

This will take months. It could take years. **I don't want to give anybody the impression that I know what I am doing.** I am an engineer by trade, yes, but I am _such_ a noob to the entire VR space and tech stack. I have no idea why I'm even doing this other than, "It's neat." I can almost guarantee that this will crash and burn. I'll hit some roadblock that will mean this project is dead. This is probably the most difficult, most expensive thing I've ever done. But I'll give it a go, so that _Other People Don't Have To™_. At least then we'll know.

Here's the plan:

1. Get it set up with my lighthouses (V1.0), and get data out of it onto my computer in _literally any_ capacity.
2. Talk to it over serial. Set up toolchain, build + flash firmware.
3. Get it talking to SteamVR.
4. Start Hacking it. Add sensors, try making my own device. Design some PCBs, print some trackers, etc.

What is the end goal, you might (and definitely should) ask? Well, I just think that SteamVR Trackers are Too Damn Expensive, and I think it would be Swell to have a single tracker cost $60. Now that I've seen how difficult this field is, I think that would be reasonable. That would still mean that my $200 pricepoint for ClearGauntlets would be tight, if not impossible, since that'd be $120 for tracking _alone_ for a pair where we originally wanted to spend no more than $50, but $25 for a tracker is almost certainly a pipe dream, at least in 2023.

In summary, I want to take Bitcraze's design and source code and turn it into a Vive Tracker That You Can Build At Home. Order the PCB, order the parts, print a case, solder it up, flash it, and you're off. A DIY tracker for $60 designed for _humans_ (not drones) to wear. That price has to include the PCB, every component on the PCB, the battery, the chassis, and any additional mounting hardware you'd need.

**Here's a list of everything off the top of my head that will be a _P R O B L E M:_**

- The FPGA (and by extension Bitcraze's board) needs EXACTLY 3.0V. **NOT 3.3V.**
- The FPGA only appears to have enough I/O for 12 TS4231's (the chip connected to the photodiode that gets pulses from the Lighthouse)
- Everything is REALLY SMALL. Seriously I ordered this board and have it in hand and MY GOD IT IS SO SMALL
- Chip shortage could completely ruin my life. I've checked DigiKey and Mouser, and they seem to have stuff in stock, but I haven't actually bought anything yet because I am a coward.
- Valve might get   **a n g e r y**   at me. (please hire me your technology is so cool)
- Bitcraze's FPGA code is written in Scala
    - I don't know Scala
        - I don't _want_ to know Scala
- I haven't a scooby how I'm actually going to get data off the board yet
    - This is actually twofold. Firstly, something-something Serial over 3.3V something-something.
    - Secondly, the LPD (Lighthouse Positioning Deck) does not have any kind of CPU onboard, only the FPGA.
        - So I need a microcontroller and that'll probably be a Lot Of Coding And Algorithms.
- I am a Bozo and a Fool and Not Very Good At Computers.

But other than that, this seems pretty easy. I've got the board here on my desk, and I'm looking at it right now... and I just realized that I'm writing this blog post to delay working on solving all of the above problems. So... guess I'm gonna go do that.