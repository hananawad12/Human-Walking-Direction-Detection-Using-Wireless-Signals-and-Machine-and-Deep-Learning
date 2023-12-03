OBJS = csi_fun.o main.o
CC = mips-openwrt-linux-gcc # gcc

recv_csi: $(OBJS)
	$(CC) $(OBJS) -o recvCSI2

csi_fun.o: csi_fun.c csi_fun.h
	$(CC) -c csi_fun.c -o csi_fun.o

main.o: main.c csi_fun.h
	$(CC) -c main.c -o main.o

clean:
	rm -f *.o recv_csi

