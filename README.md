# yager
Yager is the TEE based monitor in trustzone and could be used to monitor the behavior of Rich OS in normal world

Description:
Hardware virtualization based monitoring, like libvmi and DRAKVUF, is a good approach to provide the out-of-the-box dynamic code analysis and offer a stealthy guest instrumentation. However, the overhead of this type of monitoring is extreme high, mostly over several times. Alternatively, nearly all of the modern ARM and Intel architectures provide trusted execution environment (TEE) to offer isolated storage and execution environment, entitled as “normal world” and “secure world”. The purpose of this project is to constructure a monito(like eBPF in the latest version linux kernel) in the “secure world” which can collect sensitive data from the rich operating system( locating in the “normal world”) and create a stealthy monitor since program in “normal world” cannot access “secure world” directly. In our project we choose the trustzone on ARM (op-tee) as our TEE basement.

Reference:
1. OP-TEE: https://github.com/OP-TEE
2. eBPF: http://www.brendangregg.com/perf.html#eBPF
3. SPROBES: http://www.cse.psu.edu/~trj1/papers/most14.pdf
4. DRAKVUF: https://drakvuf.com
