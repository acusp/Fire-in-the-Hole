all: build

build:
	gcc -O3 -Wall -Wextra -ggdb -o 11013 CVE-2017-11013.c hexdump.c -lpcap -lrt
	gcc -O3 -Wall -Wextra -ggdb -o 11014 CVE-2017-11014.c hexdump.c -lpcap -lrt
	gcc -O3 -Wall -Wextra -ggdb -o 11015 CVE-2017-11015.c hexdump.c -lpcap -lrt

clean:
	rm -rf 11013 11014 11015
