######################################################################
#  Project Makefile
#
# Praveen, 30.03.2024: This example wokrs with UART interface on the bluepill board 
# 			1. First exceute make with lines 10, 11 and 18 uncommented
#			2. Comment lines 10 and 11 and Uncomment line 18 uartlib.o and exceute make
#			3. Comment lines 18 and execute make	
######################################################################

#uartlib.c: ../libwwg/src/uartlib.c
#	cp ../libwwg/src/uartlib.c ../libwwg/include/uartlib.h ../libwwg/src/uartlib.o
BINARY		= main
SRCFILES	= main.c uartlib.c rtos/heap_4.c rtos/list.c rtos/port.c rtos/queue.c rtos/tasks.c rtos/opencm3.c
LDSCRIPT	= stm32f103c8t6.ld

DEPS		= uartlib.c uartlib.h	# Any additional dependencies for your build 
#
#uartlib.o: uartlib.h
#
CLOBBER		+= uartlib.c uartlib.h	# Any additional files to be removed with "make clobber"

include ../../Makefile.incl
include ../Makefile.rtos

######################################################################
#  NOTES:
#	1. remove any modules you don't need from SRCFILES
#	2. "make clean" will remove *.o etc., but leaves *.elf, *.bin
#	3. "make clobber" will "clean" and remove *.elf, *.bin etc.
#	4. "make flash" will perform:
#	   st-flash write main.bin 0x8000000
######################################################################
