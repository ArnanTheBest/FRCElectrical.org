---
icon: lucide/plug-zap
title: Making Connections
---

# Making Connections

This page covers everything needed for you to make successful connections in the FRC Control System

## Crimping Connectors
* Molex: This is the single best connector for CAN and low AWG power wire. 
  - It’s easy to crimp, low profile, shrouded, and pin and socket. 
  - Two-pin Molex is the standard for integration into SystemCore and Adapter boards for Krakens. 
  - Using the TPA is also heavily recommended, as it raises the terminal retention from 17.5 N to 50+N, as seen in the poster. 
* Anderson: For higher AWG power wire, Anderson is the best connector. The TRIcrimp is recommended for crimping, as well as the tin-plated connectors.
* Powerpole adapter boards
  - As mentioned previously, these are boards for Krakens that convert the ring terminal outputs to Anderson and Molex.  
* Ferrules: Used for wires that connect to the ports of components like the RIO/SYSTEMCORE or PDH as well as for connections that involve linear WAGOs.
* Dupont: Dupont crimps were commonly used for Rio Connections, but are not recommended for new robots. With Systemcore, molex is recommended for connections.

### Molex 
<iframe width="560" height="315" src="https://www.youtube.com/embed/khB2-0bkj9Q?si=OKBMugaFJCiNT_xy" title="Molex Tutorial" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
  * [Crimping Molex (Guide)](https://www.molex.com/content/dam/molex/molex-dot-com/en_us/pdf/general/Final_Crimp_Poster_FIRST.pdf?inline)

### Anderson
<iframe width="560" height="315" src="https://www.youtube.com/embed/NwgLyCA1N-4?si=NxpvXeXWWQa6AiLu" title="Anderson Tutorial" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### Ferrule
<iframe width="560" height="315" src="https://www.youtube.com/embed/VYLnkpxGyCQ?si=07sZZAG_dudaspIo" title="Ferrule Tutorial" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>



<iframe width="560" height="315" src="https://www.youtube.com/embed/NSqPHQ1zQco" title="How to solder two wires together | Crutchfield" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## Solder
* Solder connections, as opposed to crimped connections, can be made for connections between wires
!!! warning
    FRCElectrical.org does not recommend soldering for FRC robots. 

### Why Soldering is Not Recommended
* They are more prone to failure under vibration and stress
* Repairing solder joints is more time-consuming and difficult in competition stress
* Solder can be poor conductor which can be brittle when done improperly
* Similarly, for newer teams, it requires more of a learning curve and practice to get right.
* Low gauge wire should not be soldered as it is usually a failure point on the robot. Refrain from soldering battery wire.
- **Solder Sleeves**: Solder sleeves are not recommended for FRC robots.
  - They use low-melting-point solder and rely on heat to both solder the wire and shrink the tubing, making it difficult to achieve a consistent, reliable connection.
  - If not heated correctly, they can create weak electrical or mechanical joints that may fail under the vibration and impacts experienced during competition.
- Properly crimped connectors are the preferred solution, while hand-soldered splices with heat shrink should only be used when a crimped connection is not practical.

### When Soldering Might Be Acceptable
* For temporary connections
* In Wiring LEDs, where you need to connect an LED strip to the CANchain (if applicable) or power
* To create custom 120 Ohm Resistors, which are used to terminate the CAN bus
* Soldering is a skill that is used in the workforce. FRCElectrical.org does not recommend it for newer teams that wish to create connections on an FRC Robot.
  * However, if you are experienced with soldering, it can be a useful skill to have (and teach!)


### Lineman's Splice
* The Lineman’s Splice also known as the [NASA Splice](https://m.youtube.com/watch?v=O-ymw7d_nYo) is probably the highest strength solder joint, and also the one with the profile best fit for heatshrink.
  * Solder sleeves (explain why not to use them: low-melt solder, which is usually low quality, and doesn't flow well. It's just as easy as normal solder splices to get wrong if you don't apply enough heat for long enough.)
* 221 Inline WAGOs & y/g WAGOs
  * Solder connections are not advised as they are fragile and do not typically stand through much strain
  * Crimp connections are recommended

### WAGO Connectors

- WAGO connectors provide quick connections without screws, solder, or crimps.
- They have two primary types: inline and Y/G.
- 221 Inline WAGOs use a lever mechanism to open and close the clamp.
- Wire enters from opposite ends to create a straight-line splice.
- Connects exactly two wires to extend in a single line.
- Y/G WAGOs use a push-in mechanism with no levers.
- They are used to bundle multiple grounding wires together.
- Wires enter from the same side to create a parallel connection.
- This image shows an inline WAGO connector.

![Inline WAGO](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR4rxyzN_EOWNZROBWW0aYcMufoc3x3eFZhPSzDbjsbtg&s=10)

- This image shows a Y/G WAGO connector.

![Y/G WAGO](https://static.grainger.com/rp/s/is/image/Grainger/2773-404__798HM9_v1?$adapimg$&hei=536&wid=536)


## Tug Test
* A tug test is a method of testing the strength of a connection
* It is recommended to perform a tug test on all connections to ensure they are secure
* This is especially important for connections that are subject to stress
* Performing tug tests on connections can help identify weak points in the robot's wiring before it is on the competition field.
* You do not need to pull as hard as possible, just enough to ensure the connection is secure.