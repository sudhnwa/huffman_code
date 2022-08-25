# huffman_code
demonstration of data compression algorithm in C

Huffman Coding is a lossless data compression technique.We generate prefix codes for each and every character encountered while reading the input file or input text.
To generate these prefix code we use tree traversing method which follows greedy algorithm.The tree is generated using characters and their frequencies.

First calculate frequency of each and every character and generate linked list, each node of linked list will contain data as charecter and it's frequency.Sort the linked list in ascending order so that nodes with characters having less frequency will be at the start of the linked list.

while executing the code it takes the three command line arguments:
  1.  The name of file, in which data to be compressed is present
  2.  The name of file, in which codes to be stored
  3.  The name of file, in which decoded data to be stored
