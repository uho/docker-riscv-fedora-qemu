FROM debian

RUN apt-get update -y &&  apt-get upgrade -y && apt-get -y install build-essential git pkg-config zlib1g-dev libglib2.0-dev libpixman-1-dev wget flex bison python paxctl
RUN git clone https://github.com/riscV/riscv-qemu

WORKDIR riscv-qemu

# RUN git checkout -b riscv-master --track riscv/master
RUN ./configure --target-list="riscv64-softmmu"
RUN make -j4 
# RUN ./riscv64-softmmu/qemu-system-riscv64 -cpu \?

RUN paxctl -c riscv64-softmmu/qemu-system-riscv64
RUN paxctl -m riscv64-softmmu/qemu-system-riscv64

RUN wget https://fedorapeople.org/groups/risc-v/disk-images/vmlinux
RUN file vmlinux

# image in volume!
# RUN wget https://fedorapeople.org/groups/risc-v/disk-images/stage4-disk.img.xz
# RUN xz -d stage4-disk.img.xz

RUN wget https://fedorapeople.org/groups/risc-v/disk-images/bbl

VOLUME /data


COPY boot.sh /boot.sh
RUN chmod 755 /boot.sh

EXPOSE 10000


CMD /boot.sh

# login: root riscv

# dnf -y install autoconf git wget libtool automake

# wget https://www.complang.tuwien,ac,at,/forth/gforth/Snapshots/current/gforth.tar.xz

# tar Jxf gforth.tar.xz

# ./autogen.sh

# ./configure


