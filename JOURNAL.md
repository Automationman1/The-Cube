---
title: "The Cube"
author: "@Automationman"
description: "Compact CoreXY Flying Gantry Printer"
created_at: "6/16/25"
---

Total time spent: 26 hours

# The Cube 6/13/2025 Day 1
## Brainstorming
After trying to make a printer that could fold for portability, and discovering that issues had popped up along the way, I decided to start work on a really small printer. I knew I wanted it to have interesting kinematics, as all the printers in my house are fixed gantry CoreXY machines, where the bed moves down. In this design however, the bed stays fixed while the gantry moves in Z, like a Voron 2.4, another flying gantry printer. The one main constraint I wanted to aim for was keeping the outer dimensions at 250mm cubed. Since I was significantly limited in volume, I had to ensure that I would have enough room to get 120mm in both X and Y on the bed, which led me to try two different iterations.

![Fitment One](https://github.com/user-attachments/assets/8f15e5fd-ae87-4ac7-8d6a-c5b417afac1a)

The version above was the first version I tried, where the gantry spans all the way to the front, allowing for maximum travel in Y. This, however severely limited my travel in X, as I would need 46mm more than if the gantry was flush with the outer perimeter (2020 is 20mm, with 3 mm of clearance on each side to get 23mm then on both sides makes 46mm). Thus I ended up going with the version below, where I lose a bit of Y in return for gaining 46mm of travel in X.

![Fitment Two](https://github.com/user-attachments/assets/7e45e45d-1ca4-4de9-bf22-e535bc92acef)

Time spent: 4 hours

## Start of Designing the Printed Parts

I ended up starting to design the front idlers of the gantry, as I knew that these would be the most complex part due to having the front Z-axis belts being routed through the XY belting. I ended up trying multiple layouts, and rotating the belts 90 degrees from there current position, however I settled on the current design picture below as it would allow me more X and Y travel along with letting the Z motors being positioned in a nice configuration for adding elecronics.

![Gantry with Front Idlers](https://github.com/user-attachments/assets/2c9c67de-e0a3-45e9-9b81-0221a64c81a9)

I  also designed the front top Z idlers as they were an easy thing to knock out and I needed them anyways.

Time spent: 8 hours

# The Cube 6/14/2025 Day 2

Today I started designing the rear motor mounts for the gantry, as I knew that it would include the tensioning done by shifting the motors along with housing the rear Z axis tensioner. Ensuring that I would still get the full 120mm of Y travel was a pain though, as I had to significantly modify the rear belt path to allow for no Y loss.

<img width="611" alt="Designing the Rear motor mounts" src="https://github.com/user-attachments/assets/20ea4e78-ec64-43bc-b6b6-1a5ff5ddac58" />

Time spent: 5 hours

# The Cube 6/16/2025 Day 3
## Starting the Repo
I started off the day by creating the Github repository, and setting up the journal.

Time spent: 2 hours

## Progress on Electronics

After taking a break, I started researching the electronics I was using to ensure compatibility and compactness within the build volume. Initial my plan was to use a SKR v1.4 with a standard sized RaspberryPi. After some test fitting in CAD, I knew this would not work. I also knew that I did not want to add a separate 5v PSU for the RPi as that would take up more space than I even had, so I looked into BigTreeTech's BTT Pi, a Pi like SBC that is design for 3D printers so it can take in 24v directly. Since I was test fitting and still discovered that this would not fit, as it was still the same size as an RPi, I looked to the Pi Zero 2 W as a more compact alternative. I knew that it would have less standard ports however that was made up for in it's compactness. Using the RPi Zero 2 W, I was able to save significant space, allowing me to have room for wiring and to keep the constraint of 250mm cubed. Shown below is the current progress on electronics fitment:

<img width="306" alt="Electronics Config 1" src="https://github.com/user-attachments/assets/82c448f2-e7d9-419f-8042-26ed54beacd0" />

Time Spent: 3 hours

## Gantry Update

I ended up cadding the XY joints for the gantry, which ended up being troublesome as I needed to ensure that the front gantry idler would have enough clearance with the joints. I also swapped from a front mounted rail to a top mounted rail to save space, as otherwise I would have needed to cram the front idler even more. Since the belt routing is similar to CloakedWayne's Monolith Gantry, I was able to find a nice and easy to modify [carriage](https://www.printables.com/model/1021158-archetype-carriage-for-monolith-with-gustav-railwa) that I could use as the base of my toolhead. This allowed me to swap it to a top rail, as I knew that the Voron V0 has a printed carriage that prints in a similar fashion to this so I knew that it would be rigid enough. 

<img width="510" alt="Toolhead Carriage" src="https://github.com/user-attachments/assets/2f4405ab-5de0-4ceb-92e1-a187c3a06568" />

<img width="503" alt="XY joint" src="https://github.com/user-attachments/assets/4dafa517-f546-4326-a622-3f3d24e659ca" />

Time spent: 4 hours
