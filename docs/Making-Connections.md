---
icon: lucide/plug-zap
title: Making Connections
---

# Making Connections

This page covers everything needed for you to make successful connections in the FRC Control System.

## Crimping Connectors

- **Molex Connectors**: These are the preferred choice for CAN and high AWG power wire.
- The most common type of Molex connector in FRC is the Molex SL series, though other variants are also sometimes used.
- They are low-profile, shrouded connectors available in pin and socket configurations, making them easy to assemble and highly reliable. Their housings also contain latches, which ensure secure connections.
- Two-pin Molex SL is the standard for integration into SystemCore and Adapter boards for Krakens.
- Using the TPA is also heavily recommended, as it raises the terminal retention from 17.5 N to 50+N, as seen in the poster.
- This image shows the Molex SL connector.

![Molex SL](/assets/making-connections/Molex_SL.png)

- **Anderson Connectors**: For lower AWG power wire, Anderson connectors are the preferred choice, with SB50 for battery wires and Powerpole for 10-12 AWG wires.
- The TRIcrimp is recommended for crimping, as well as the tin-plated connectors.
- This image shows the Anderson SB50 connector.

![Anderson SB50](/assets/making-connections/SB-50.png)

- This image shows the Anderson Powerpole connector.

![Anderson Powerpole](/assets/making-connections/Anderson-Powerpole.png)

- **Powerpole Adapter Boards**
- These boards convert Kraken ring-terminal outputs into Anderson Powerpole and Molex SL connections, making wiring cleaner and easier to service.
- This image shows the Powerpole adapter board.

![Powerpole Adapter Board](/assets/making-connections/Powerpole-Adapter_Board.png)

- **JST**: JST connectors are commonly used for low-current signal wiring.
- These can be found in sensors, encoders, LEDs, and other low-power devices.
- Their compact polarized design helps keep them organized while preventing incorrect connections.
- The most common type of JST connector in FRC is the JST-PH series.
- This image shows the JST-PH connector.

![JST-PH](/assets/making-connections/JST.png)

- **Ferrules**: Ferrules are used for stranded wires that connect to the ports of components like the RIO or PDH as well as for connections that involve linear WAGOs.
- They prevent stray wires from causing short circuits.
- This image shows a ferrule.

![Ferrule](/assets/making-connections/Ferrule.png)

- **Dupont**: Dupont crimps were commonly used for roboRIO connections, but are not recommended for new robots. With Systemcore, Molex SL is recommended for connections because of its locking latches that prevent wires from accidental disconnections.
- This image shows a Dupont connector.

![Dupont](/assets/making-connections/Dupont.png)

### Molex SL

<iframe width="560" height="315" src="https://www.youtube.com/embed/khB2-0bkj9Q?si=OKBMugaFJCiNT_xy" title="Molex SL Tutorial" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

- [Crimping Molex SL (Guide)](https://www.molex.com/content/dam/molex/molex-dot-com/en_us/pdf/general/Final_Crimp_Poster_FIRST.pdf?inline)

### Anderson Powerpole

<iframe width="560" height="315" src="https://www.youtube.com/embed/NwgLyCA1N-4?si=NxpvXeXWWQa6AiLu" title="Anderson Powerpole Tutorial" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### Anderson SB50

<iframe width="560" height="315" src="https://www.youtube.com/embed/eKJlXt2ZUEc" title="Crimping Anderson SB50 connectors" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### Ferrule

<iframe width="560" height="315" src="https://www.youtube.com/embed/VYLnkpxGyCQ?si=07sZZAG_dudaspIo" title="Ferrule Tutorial" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## Solder

- Solder connections, as opposed to crimped connections, are sometimes weaker and less reliable.

!!! warning
    They are HEAVILY discouraged for teams, and especially newer teams. The reason that teams usually go this route is that they’re seen as equivalent to a continuous run. In fact, soldering is a failure point on the bot, and like connectors, it needs to be properly strain relieved.

- Soldering is relatively easy once it's learned, but there is a learning curve, as well as more room for error than crimped connectors. Additionally, in an FRC environment it’s fast paced, if something breaks or needs to be replaced it’s extremely challenging.
- Solder connections are not advised as they are fragile and do not typically stand through much strain.
- Crimp connections are recommended.
- **Solder Sleeves**: Solder sleeves are not recommended for FRC robots.
- They use low-melting-point solder and rely on heat to both solder the wire and shrink the tubing, making it difficult to achieve a consistent, reliable connection.
- If not heated correctly, they can create weak electrical or mechanical joints that may fail under the vibration and impacts experienced during competition.
- Properly crimped connectors are the preferred solution, while hand-soldered splices with heat shrink should only be used when a crimped connection is not practical.

<iframe width="560" height="315" src="https://www.youtube.com/embed/NSqPHQ1zQco" title="How to solder two wires together | Crutchfield" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### Lineman's Splice

- The Lineman’s Splice, also known as the [NASA Splice](https://m.youtube.com/watch?v=O-ymw7d_nYo), is probably the highest-strength solder joint, and also the one with the profile best fit for heatshrink.
- This image shows a Lineman's Splice.

![Lineman's Splice](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcStPf7v3-vjRNrUF57WlSFXMmlLrr-nmK5hW_IlodEm_Q&s=10)

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