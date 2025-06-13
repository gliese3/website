---
author: "Evgenii"
title: "Group meeting 06/11/2025"
date: "2025-06-11"
description: ""
FRtags: ["EQSL", "group meeting"]
ShowToc: true
TocOpen: false
---

## Attocube stack thermolization
### Adding copper braids

- <span style="color:orange;">_problem_</span>: temperature on top of the Attocube stack is high (**~25K**) for Ne deposition
- made several attempts to lower the temperature (adding copper braids)
{{< figure src="images/IMG_20250506_164552.jpg" title="manually made copper braids">}}
{{< figure src="images/IMG_20250520_183941.jpg" title="setup with copper braids (1)">}}
{{< figure src="images/IMG_20250520_183945.jpg" title="setup with copper braids (2)">}}

- this configuration allowed us to lower the temperature up to **13K**, but the rotational movement was limited to about 90°, which is not sufficient for the proposed optical setup. Although the braids connected to the rotor are very thin

- <span style="color:blue;">_note_</span>: when start moving stages, temperature could increase by several Kelvins


### Using copper plate

- machined a 0.5 mm thick copper plate from OF copper stock and soldered copper braids
{{< figure src="images/IMG_20250523_192406.jpg" title="machined copper plate">}}
{{< figure src="images/IMG_20250527_134333.jpg" title="installed copper plate with braids">}}

- experiment with the plate revealed a temperature of approximately **~19K**, which is about 5K smaller


### New copper base plate for the rotator

- as even very thin copper braiding could prevent the stage from rotating, the idea is to try manufacturing a new copper base plate for the rotator with holes for the copper braiding. The new copper base plate could be thermally insulated from the XYZ-stack by a PEEK plate
{{< figure src="images/sketch.png" title="machined copper plate">}}
{{< figure src="images/image (1).png" title="CAD model of the new plate">}}
{{< figure src="images/IMG_20250601_191404.jpg" title="machined plate using lab CNC">}}
- an order has been placed in an outsourcing CNC company

## Copper electropolishing

- did quick experiments on copper electropolishing using phosphoric acid
{{< figure src="images/IMG_20250607_143715.jpg" title="bare and electropolished plates">}}

## First ablation experiments

- Tm ablation in ambient atmosphere
{{< figure src="images/IMG_20250610_155329.jpg" title="sample BEFORE ablation">}}
{{< figure src="images/IMG_20250610_160545.jpg" title="sample in microscope BEFORE ablation">}}

{{< figure src="images/IMG_20250610_161921.jpg" title="sample AFTER ablation (4 pulses at almost max power)">}}
{{< figure src="images/IMG_20250610_162603.jpg" title="sample in microscope AFTER ablation 4 pulses at almost max power">}}

- stainless steel ablation
{{< figure src="images/IMG_20250610_181637.jpg" title="stainless steel washer in microscope AFTER ablation 3 pulses at almost max power">}}

## Attocube stack temperature measurments

- measured temperature of different positioners in the stack at different conditions. Used varnish and capton tape to mount temperature sensor (Cernox)
{{< figure src="images/IMG_20250602_165907.jpg" title="z-stage temperature measurment">}}
{{< figure src="images/2025-06-12_11-37.png" title="log file of cooldowns">}}

- temperature gradient is significant

## Laser ablation theory

- the phase composition of the removed material strongly depends on the laser fluence
{{< figure src="images/2025-06-12_11-54.png" title="material removal model calculated for Al ">}}

- laser beam interacting with matter could lead to extraction of atoms, clusters and even droplets from the target material. These
generated particles heave an initial speed that could reach values of tens of kilometers per second but is gradually decreasing while interacting with ambient atmosphere

- fundamental criteria for choosing certain irradiation conditions for high quality ablation of a given material consists mainly of relation between the ablation rate and the thermal and optical penetration depths
{{< figure src="images/2025-06-12_12-11.png" title="craters with 100 microns diameter drilled in steel in vacuum">}}

- for the _ns_ and _ps_ pulses the image indicates the presence of the molten material around the crater whereas for the _fs_ pulses there is no evidence of molten material but only a vapour dust ring around the crater
{{< figure src="images/2025-06-12_12-15.png" title="temporal evolution of the vapor plume after irradiation">}}
{{< figure src="images/2025-06-12_12-16.png" title="precision depending on pulse duration">}}

- physics of the ablation process is complex, given that it involves laser-solid interactions, the vapour/plasma formation and expansion, and the laser-plasma interaction

- femtosecond and picosecond laser pulses can be considered as a direct solid-vapour transition

- in nanosecond laser heating of metals the absorbed laser energy first heats up the target to the melting point and then to the vaporization temperature. In
this case evaporation occurs from the liquid metal, and heat conduction into the solid target is the main source of energy loss

- in a metal, the free electrons absorb energy from the laser and at femtosecond time scale the energy is re-distributed among the electrons by
electron-electron collisions leading to the thermalization of the electron gas

- the energy exchange between electrons and the lattice is governed by electron-phonon collisions and will last much longer (typically a few tens of picoseconds) than the thermalization of the electron gas due to the large mass difference of electrons and phonons

- under nanosecond laser pulses, the absorbed laser energy first heats the target surface to the melting point and then to the vaporization temperature. In case of metals, much more energy is needed to vaporize than to melt the material

- in the case of laser ablation with ‘long’ nanosecond laser pulses there is enough time for the thermal wave to propagate into the target and to create a relatively large layer of melted material. In this case the evaporation occurs from the liquid metal, which makes accurate material processing of metal targets with nanosecond pulses very difficult

- the laser-ablation process can be divided in two stages: (a) evaporation of the solid target and plasma formation; (b) expansion of the ablated plume in vacuum or into the surrounding medium

- in the case of nanosecond laser ablation of metals in vacuum, for fluences higher than a threshold value which is about 2 J/cm2 (0.5 J/cm2 for our laser @532 nm), a plasma is always produced above the target surface

- at higher fluences the vapour temperature is high enough to produce important ionization of the ablated species so that the vapour begins to absorb the incident laser radiation leading to vapour breakdown and plasma formation

- the simplest approximation of the ablation plume is a mixture of ionized and neutral atoms, the ions usually representing less that 5 % of the total number of atoms
{{< figure src="images/2025-06-12_12-42.png" title="plume particles interaction with reflector">}}

- big particles will reach the substrate area much later (microseconds) than the plume fine particles. Solution was to correlate a shutter with the laser pulse and to close it after the first part of the plume, containing the ‘fine’ particles, is passing the shutter
{{< figure src="images/2025-06-12_15-25.png" title="shutter filtering experimental setup">}}

- using experimental setups with particular geometries for speculating differences of different particles interactions with obstacles and with each others is
one approach widely use for the plume filtering

- axe-off deposition: the base of this technique is the idea that the fine particles of the plume will have a ‘fluid like’ behavior due to interactions with each other and with the ambient gas molecules, while the large (and heavy) particles of the plume will usually have a linear trajectory, due to their mass. Particles could be deposited only by being deviated from their linear trajectories
{{< figure src="images/2025-06-12_15-36.png" title="filtering techniques">}}

- back-side deposition
{{< figure src="images/2025-06-12_15-41.png" title="back-side deposition">}}

- plane mask technique
{{< figure src="images/2025-06-12_15-44.png" title="plane mask technique">}}
{{< figure src="images/2025-06-12_15-45.png" title="plane mask technique example">}}

- plume reflection technique
{{< figure src="images/2025-06-12_15-46.png" title="plume reflection technique">}}

- quartz microbalance to monitor ablation
{{< figure src="images/2025-06-12_15-49.png" title="quartz microbalance">}}






