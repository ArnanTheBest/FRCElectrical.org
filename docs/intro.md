---
icon: lucide/play
title: Intro to FRC Electrical
---

# Intro

## Safety
This may come as a shock, but electronics are dangerous. A single mistake could lead to serious injury, and it is vital to learn how to follow proper procedure when handling electronics.

- A battery spilling is dangerous for everyone because it can cause chemical burns and damage if you touch it. When a battery spills, cover it with baking soda. This neutralizes the battery acid and it becomes less harmful. Do **not** touch your eyes until after washing your hands.
- Never hold batteries from the wires. Always hold them from the body. By holding batteries from their wires, you are wearing down the connection between the wire and the battery which can be detrimental for performance. This can also lead to a snap in the batteries terminal, which can drop the battery if you're holding it.
- Always wear PPE when handling electronics. This includes at the bare minimum safety glasses. 
- Don’t touch the metals of opposite polarity wires together, especially for batteries as it can cause sparks and flame.
- Don’t allow metal shavings to get into components: Use electrical tape to cover open holes in components. This prevents short circuits and damage to sensitive parts.
  - A short circuit is when two wires with different polarities have contact, causing a large current to flow and potentially causing fire or damage to components.
- Keep exposed wires away from things that can break them like motor splines or the insides of swerve modules. This prevents damage to the wires and potential short circuits.
  - Always try and keep your wiring mounted on the robot and away from the motion of your and other robots.

## Electrical Theory
While electrical isn’t overly complex and the theory is rarely used in FRC electrical, a basic understanding is good to know.

### Voltage, Current, and Resistance
- The standard definition is the difference in electric potential between two points. However, this is hard to imagine visually. Think of a wire as a pipe, and the electrons flowing through it as water. Voltage would be the water pressure. It is measured in Volts (V), where a higher voltage means more pressure/potential.
- Current, in this analogy, would be the rate at which water flows through the pipe. It is the flow of electrons going through the wire measured in Amps (A).
- Resistance can be thought of as blockages in this pipe or as points where it gets narrow. It is the resistance of the flow of electrons measured in Ohms (Ω) that slows the electrons from getting from point A to point B.
- Ohm's Law: $V = I \cdot R$ where $V$ is voltage, $I$ is current, and $R$ is resistance.

### Power vs. CAN vs. PWM vs. I2C
- Power wire is red (for positive terminals) and black (for negative and ground terminals). FRC power wires MUST be color-coded separately, as they can be dangerous when not indicated. Red and black are the most common ways to do so. They can be thought of as the blood vessels that deliver power to every part of the robot. 
- CAN Wire can be any two colors, but they are most commonly green and yellow. This color scheme can be changed to most anything to differentiate between different CAN buses. CAN is essentially the robot's information system. If the power wires are the blood vessels, CAN is the nervous system. 
    - Differential Buses: CAN is a differential bus. This means that it essentially transfers information by measuring the voltage difference between two wires in a pair (CAN High (Yellow) and CAN Low (Green)). This makes it more resistant to noise, or electromagnetic interference (EMI), which is prevalent in FRC. However, some measures need to be taken for this noise resistance to be most effective:
        - Twist the wire pairs: We do this because it allows any external vibrations and EMI to affect both wires rather than one, keeping the measurements on each wire consistent with each other.
        - Strain relief: Strain relief is when you give wiring to a strong component that eliminates the potential of a stronger, unintended force, from pulling on the wire. This way, the strain is pulling on the component instead of the wire's connector. This is important in any system, whether power or CAN.
- PWM: "Pulse-Width Modulation" - one-wire signaling to send any value between 0-100%
    - Systemcore contains 6 PWM ports via Smart I/O
- I2C (pronounced eye-squared-see or eye-two-see): "Inter-Integrated Circuit" - two-wire signaling to send any value between 0-100%
    - Systemcore contains 6 PWM ports via Smart I/O

=== "CAN Wiring"
    ![CAN-Wiring](/assets/FRC-Control-System/CAN-Wiring.png){ width="50%" }
=== "Power Wiring"
    ![Power-Wire](/assets/FRC-Control-System/Power-Wire.png){ width="50%" }

### AWG (American Wire Gauge)
- AWG is a standard for measuring wire gauge in the United States.
- The lower the AWG number, the thicker the wire.
- Thicker wires can carry more current and have less resistance.
- When choosing wire gauge, consider the current capacity and voltage drop and ensure that the wire you choose follows the guidelines depending on the application
  - In FRC, your thickest wire is somewhere between 2-6 AWG. This is typically used for battery connections.
    - These wires carry high current and need to be thick to handle the load.
  - For smaller components, you'll typically see 18-22 AWG wires (CAN, PWM, etc)
    - These wires carry lower current and can be thinner.
  - Other components, like motors, will typically have 8-12 AWG wires.

### Parallel vs Series
#### Parallel
- Negative to Negative and Positive to Positive. This allows for multiple paths for current to flow, increasing the total current capacity.

#### Series
- Components are chained together from positive to negative to positive, etc. The flow of electricity is the same through all components, but the voltage is divided among them. 


![Parallel-Series-Circuit](/assets/Intro to FRC Electrical/Parallel-Series-Circuit-Light.png#only-light)
![Parallel-Series-Circuit](/assets/Intro to FRC Electrical/Parallel-Series-Circuit-Dark.png#only-dark)
