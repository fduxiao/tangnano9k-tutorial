# Tangnano9k Tutorial

available in languages below  
[:uk:](README.md) [:cn:](README_zh.md)

Recently, I have bought a [Tangnano9k board](https://wiki.sipeed.com/hardware/en/tang/tang-primer-20k/primer-20k.html) and decided to learn FPGA. 
Though I also bought a Xilinx Zynq board for a more hardcore learning, this board is a much cheaper choice and open source tools for it can be found so that I can program the board on my Macbook, only with a Type-C cable.

The reason I want to write the tutorial is that I cannot find any tutorial on this board. 
The manufacturer, Sipeed, only provides some naive tutorial based on Gowin IDE, which requires you to apply a licence from Gowin. 
After doing some search, I finally found [Yosys](https://github.com/YosysHQ), a very sweet toolchain.

I aim to provide a gentle introduction to FPGA for newbies just like me who have bought the board but do not know what to do with it, so I may give the tutorial in a silly way, describing digital circuits with my own understanding. 
Since my major is mathematics, I may make a lot of mistakes in this tutorial. I hope that you could correct me by making pull requests (including my English).

I think FPGA is a very suitable target language for code generator especially for simulation, 
so the tutorial is going to develop a meta-language model for verilog. 
I will not write too many testbench files for simulation. Instead this
should be done in the meta-language model. I choose [Python](https://www.python.org) as the meta-language. You can freely choose any language you like (coq is a very nice choice, but for pedagogical reason, I had better not use it). 
As in [SICP](https://mitpress.mit.edu/9780262510875/), I will describe the *behavior* of the model in meta-language. If you want to fulfill it
with other languages, be sure to understand what I want to do (in the python code) and write your code in an idiomatic way. 
(Do not merely translate python into your favorable language.) 

## Preparations
