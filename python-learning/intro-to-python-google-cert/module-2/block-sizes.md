---
description: The program focuses on returning block sizes
---

# Block Sizes

### Problem

**If a filesystem has a block size of 4096 bytes, this means that a file comprised of only one byte will still use 4096 bytes of storage. A file made up of 4097 bytes will use 4096\*2=8192 bytes of storage. Knowing this, can you fill in the gaps in the calculate\_storage function below, which calculates the total number of bytes needed to store a file of a given size?**



```
def calculate_storage(filesize):
	block_size = 4096
	full_blocks = filesize // block_size
	partial_block_remainder = filesize % block_size
	if partial_block_remainder > 0:
		return (full_blocks*block_size + block_size)
	else:
		return full_blocks*block_size

print(calculate_storage(8192))
```

