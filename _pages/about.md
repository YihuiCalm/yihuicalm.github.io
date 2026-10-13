---
layout: about
title: about
permalink: /
subtitle: Ph.D. Student · <a href='https://ece.umd.edu/'>ECE, University of Maryland</a> · <a href='https://sites.google.com/umd.edu/shahlab'>Shah Lab</a>

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <p>Me and my RAs (Jojo & Wuhua)</p>

selected_papers: true # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page

announcements:
  enabled: false # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

I am a Ph.D. student in Electrical and Computer Engineering at the University of Maryland, College Park, advised by [Dr. Sahil Shah](https://ece.umd.edu/clark/faculty/1398/Sahil-Shah). I work on **energy-efficient neuromorphic hardware**: clockless (asynchronous) circuits and sparsity-aware networks-on-chip for spiking neural networks, carried all the way to silicon.

I have taped out two chips as lead digital designer: [SpineLink](/projects/spinelink_tapeout/), a 32-neuron fully asynchronous spiking-neural-network chip with a tree-spine network-on-chip (TSMC 180 nm, June 2026), and a synthesizable asynchronous AER encoder (TSMC 65 nm, 2025) whose silicon measurements, 33 MEvent/s at 435 fJ per event, are published at IEEE MWSCAS 2026. Along the way I developed a method for closing timing on bundled-data asynchronous logic inside a standard Genus/Innovus flow, which is [open source](https://github.com/YihuiCalm/Automated_Async_Bundled-Data_Synthesis_Flow).

I am part of the ARO MURI on [hybrid artificial-living neural networks](https://hybrid-ai.umd.edu/about/) led by Prof. Wolfgang Losert, which seeks to identify the learning rules of biological neurons and replicate them in silicon. My contribution is the hardware readout, an [FPGA spiking decoder](/projects/lif_decoder_fpga/) that reads a simulated neuron culture at 9.2 pJ per synaptic operation (npj manuscript under review).

Before Maryland, I completed my M.S. at George Washington University, where I implemented spiking neural networks on FPGA and got hooked on neuromorphic systems. I hold a B.Eng. from Yanshan University in China.

I like building tools that other people can use. My [Digital Design Flow](https://github.com/YihuiCalm/Digital_Design_Flow) scripts (used for both tapeouts) and [Izhikevich Neuron FPGA](https://github.com/YihuiCalm/IZ_Neuron_FPGA) implementation are open source on GitHub. The current [resume](/assets/pdf/CV.pdf) is on the CV page.

When I'm not in the lab, I'm probably being supervised by Jojo and Wuhua.
