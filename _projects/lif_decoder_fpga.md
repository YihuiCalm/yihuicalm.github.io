---
layout: page
title: FPGA spiking decoder
description: Real-time LIF decoder for hybrid biological-artificial networks (npj manuscript under review)
img: assets/img/publication_preview/lif_decoder_demo.gif
importance: 2
category: chips
related_publications: true
---

The hardware readout for our hybrid biological-artificial computing study with the Losert lab: a spiking-neural-network decoder that classifies the responses of a simulated neuron culture and identifies the readout timescale that carries the most information.

<div class="row justify-content-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/publication_preview/lif_decoder_demo.gif" title="Live classification demo" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Live demo: the decoder on a Digilent Arty S7-50 classifies MNIST digits presented to the simulated culture in real time.
</div>

**Design.** 811 inputs to 10 leaky-integrate-and-fire neurons, 10-bit Q6.4 membrane, 4-bit weights, a 3-stage pipeline that processes one event per clock at 100 MHz, and a 6 Mbaud UART link with self-synchronizing frames. The neuron matches the snnTorch Leaky model bit for bit.

**Results.** 97.9% classification accuracy against 97.7% for the floating-point reference, 9.2 pJ per synaptic operation (post-route, SAIF-annotated), 1,323 LUTs, 720 flip-flops, no DSP slices, and it sustains 1.5× the culture's peak event rate. Source, testbenches and the bit-accurate Python model are on [GitHub](https://github.com/YihuiCalm/LIF_Decoder_For_Reservior_Computing_on_FPGA).
