1) Used the riscv64-unknown-elf-objdump tool to dump the code.
2) Find unique instructions like addi,auipc,sub,etc. List of unique commands can be obtained by using - cat dump.txt | awk '{print $3}' | sort | uniq in terminal.
3) Copied the instructions with their 32 bit codes onto a text file.
