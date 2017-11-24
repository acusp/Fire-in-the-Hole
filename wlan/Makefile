all: build

build:
	gcc -O3 -Wall -Wextra -ggdb -o poc CVE-2017-xxxx.c hexdump.c -lpcap -lrt

clean:
	rm -rf poc
