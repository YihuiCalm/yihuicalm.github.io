---
layout: page
title: SpineLink tapeout
description: 32-neuron fully asynchronous spiking-neural-network chip, TSMC 180 nm, taped out June 2026
img: assets/img/spinelink_layout_card.jpg
importance: 1
category: chips
related_publications: true
---

SpineLink is a clockless hybrid network-on-chip for spiking neural networks. Four binary-tree clusters of eight neurons (seven 3-port routers each) hang off a bidirectional linear spine of two 4-port routers, so a spike is broadcast and converged inside the network with no routing tables, and chips chain over 3-wire asynchronous serial links.

The test chip was taped out in TSMC 180 nm in June 2026 on a 1 mm² die. I was the lead digital designer: RTL for the routers, synaptic memories and asynchronous SerDes; synthesis and place-and-route in Cadence Genus and Innovus; post-route SDF simulation in Xcelium; integration of the 0.36 mm² digital core (21.5k instances) with 32 analog leaky-integrate-and-fire neurons in Virtuoso; and full-chip Calibre DRC/LVS with dummy fill.

<div class="row justify-content-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/publication_preview/spinelink_layout.jpg" title="SpineLink chip layout" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    Chip layout before dummy fill: the notched digital core with 18 micropipeline routers and 1,152 three-bit latch synapses, the 32 analog neurons, and the pad frame.
</div>

**Post-layout results.** 3.8 ns and 17 pJ per 3-port router hop (5.8 ns and 32 pJ for a 4-port spine router), 1.9 µW digital static power, and 412 fJ of analog energy per spike. At 1,024 neurons the tree-spine topology needs 2.9× less router area than a 2-D mesh (6.5 vs 18.6 mm²) and 17 vs 48 nJ per broadcast spike. Silicon characterization is in progress.

The chip is the hardware side of the [ARO MURI on hybrid artificial-living neural networks](https://hybrid-ai.umd.edu/about/), which seeks to identify the learning rules of biological neurons and replicate them in silicon spiking networks.
