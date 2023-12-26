# Escalade (French for "climb", specifically mountain climbing)

![alt text](https://github.com/OldGuyMeltsPlastic/Escalade/blob/main/images/Escalade_Full_Frontal_View.jpg?raw=true)

Escalade is an Annex Engineering K3 printer with a few twists, just because I can.

After attending the Rocky Mountain Rep Rap Festival (RMRRF) in Loveland, CO in April 2023, I came back home to Ottawa, Canada and ordered myself a K3 kit from Fabreeko.

Fabreeko had a K3 on display at their booth, and the design and overall build quality just blew me away.
Another attendee @OB1Kenobi from the Annex Engineering Discord server, had also brought his own K3 build to the event, and he had a sidepack mounted on the right with a Waveshare 7.9" HDMI display mounted vertically.
I was inspired to do something similar with my own K3 build.

I have created a K3 playlist on my YouTube channel and documented most of the physical build there:
https://www.youtube.com/playlist?list=PLngLOesYVWnwKW8zaA5v_0eK2fdAM9LTv<br>
I have also created a build log on the Annex Engineering Discord server here:
https://discord.com/channels/641407187004030997/1180948550843117720

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

My configuration with the stock toolhead has a Phaetus Dragon UHF hotend, a Beacon Rev D probe, and a K3rabiner toolhead PCB. The mount parts that I found for this toolhead configuration move the hotend cooling fan to the "back" of the hotend, which leaves the front of the hotend more easily accessible for removing the silicone sock and/or swapping nozzles. Printed parts required for this toolhead configuration were collated by @ChristianN on the Annex Engineering Discord Server here: https://discord.com/channels/641407187004030997/1139276599645179946

I sourced a Waveshare 7.9" DSI display, instead of the Waveshare 7.9" HDMI display. The screw holes configuration to mount the DSI and HDMI are different from each other. I ended up having to take Minsekt's original HDMI display mount, and as no CAD was available, I hacked it apart in PrusaSlicer to get something close to functional for my DSI display.
Minsekt's mount for Waveshare 7.9" HDMI displays: https://github.com/Annex-Engineering/Annex-Engineering_User_Mods/tree/main/Printers/K3/Minsekt-K3_WaveshareScreen
OGMP's mount for Waveshare 7.9" DSI displays: https://www.printables.com/model/691631-annex-engineering-k3-sidepack-waveshare-79-dsi-mou

I am using an Arducam IMX519 Pi Cam V3-compatible camera connected to the Raspberry Pi 4B via FFC. I used Ryan-G's Outside Camera Mod and airox's rpi camera mod to mount it in the sidepacks large top middle grommet hole.
https://github.com/Annex-Engineering/Annex-Engineering_User_Mods/tree/main/Printers/K3/Ryan_G-K3_Outside_Camera
https://github.com/Annex-Engineering/Annex-Engineering_User_Mods/tree/main/Printers/K3/airox-rpi-mount-for-camera-mod-ryan

I also had to adjust the positions of the Z-Tilt probe points accordingly. Note that the Z motors and bed assembly retain their original mount points per a stock build.

Also, when mounting the front door panel to the hinges, the build instructions recommended using an M3 SHCS and a 1 mm washer/spacer inside the door panel. I found that this would cause the Z2 kinematic bed mount, which now sits at the front left of my build space, to bump into those screws at the bottom of the door, so I replaced the M3 SHCS + washer with an M3 BHCS and no washer. The door is just as secure, but now the Z2 kinematic bed mount has clearance to move up and down unobstructed.

While the K3 is now printing, I am working through resolving some pretty bad print artifacts that appear to be caused by a physical problem with the gantry motion system. Once I have corrected these, I will share my configuration and slicer settings for reference.

To mount the electronics in my K3 sidepack, I asked my friend Fizzy, creator of the Electronics Mounting System (EMS) that is popular with many Voron printer builders, to create an EMS frame for the K3. I will update with a link to it here once he has published it on Printables.

Many thanks to all of the greatly helpful people on the Annex Engineering and Fabreeko Discord servers for all of their assistance and timely responses to my many questions. This printer build would have been much more work on my part without all of the help that I received.
