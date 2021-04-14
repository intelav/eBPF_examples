# eBPF_examples
eBPF allows to write programs in pseudo assembly language and change the Linux kernel behavior on run time.

### xdp-examlpe.c is a sample program written in eBPF Virtual machince format where packets on XDP patch could be dropped by linux kernel  if applied below command in sequence 
####clang -O2 -Wall -target bpf -c xdp-example.c -o xdp-example.o
####sudo ip link set dev <network-interface>  xdp obj xdp-example.o
