# eBPF_examples
eBPF allows to write programs in pseudo assembly language and change the Linux kernel behavior on run time.
One good use case for eBPF programs could be good tool to implement FPGA accelerations on SSD/NVMe devices as mentioned on [SNIA Computational Storage](https://www.snia.org/sites/default/files/technical_work/PublicReview/SNIA-Computational-Storage-Architecture-and-Programming-Model-0.5R1.pdf) and these accelrations can be accomplised via ONEAPI tool as mentioned on Chapter 10 of [DPC++](https://link.springer.com/content/pdf/10.1007%2F978-1-4842-5574-2.pdf)

### xdp-examlpe.c is a sample program written in eBPF Virtual machince format where packets on XDP patch could be dropped by linux kernel  if applied below command in sequence 
#### clang -O2 -Wall -target bpf -c xdp-example.c -o xdp-example.o
#### sudo ip link set dev network-interface  xdp obj xdp-example.o
