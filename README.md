# Escalade

After attending the Rocky Mountain Rep Rap Festival (RMRRF) in Loveland, CO in April 2023, I came back home to Ottawa, Canada and ordered myself a K3 kit from Fabreeko.

Fabreeko had a K3 on display at their booth, and the design and overall build quality just blew me away.
Another attendee had also brought their own K3 build to the event, and they had a sidepack mounted on the right with a Waveshare 7.9" HDMI display mounted vertically.
I was inspired to do something similar with my own K3 build.

```
Original K3 configuration:

|------------------------|
|        BACKPACK        |
|------------------------|
| Y  |    | Z1 |    | X1 |
|-----    ------    -----|
|                        |
| ------          ------ |
| | Z  |          | Z2 | |
| ------          ------ |
|-----              -----|
| X  |              | Y1 |
|------------------------|

My K3 configuration:

|------------------------|----|
| Y  | Z  |         | X1 |    |
|----------         |----|    |
|                        |    |
|                 ------ |SIDE|
|                 | Z1 | |PACK|
|                 ------ |    |
|----------         -----|    |
| X  | Z2 |         | Y1 |    |
|------------------------|----|
```

For my build, it wasn't enough to rotate the printer so that the backpack now sits on the right side, but I also ended up swapping the X and Y axes so that X still moves left to right, and Y still moves front to back in the rotated configuration.

To be clear, the back/sidepack still sits on the original rear side of the printer, but the front door has been moved right, replacing the original right panel, and the right panel has moved left, replacing the original front door.

My configuration with the stock toolhead also has a Dragon UHF hotend, and the mount parts that I found for it move the hotend cooling fan to the "back" of the hotend, which leaves the front of the hotend easily accessible for removing the silicone sock and/or swapping nozzles.

I had to adjust the positions of the Z-Tilt probe points accordingly.

Also, when mounting the front door panel to the hinges, the build instructions recommended using an M3 SHCS and a 1 mm washer/spacer inside the door panel. I found that this would cause the Z2 kinematic bed mount, which now sits at the front left of my build space, to bump into those screws at the bottom of the door, so I replaced the M3 SHCS + washer with an M3 BHCS and no washer. The door is just as secure, but now the Z2 kinematic bed mount has clearance to move up and down unobstructed.
