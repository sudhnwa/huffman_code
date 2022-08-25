# huffman_code
demonstration of data compression algorithm in C

Huffman Coding is a lossless data compression technique.We generate prefix codes for each and every character encountered while reading the input file or input text.
To generate these prefix code we use tree traversing method which follows greedy algorithm.The tree is generated using characters and their frequencies.

First calculate frequency of each and every character and generate linked list, each node of linked list will contain data as charecter and it's frequency. Sort the linked list in ascending order so that nodes with characters having less frequency will be at the start of the linked list.

Tree Generation:
The tree is generated from leaf nodes to root node.
For Tree genration we have to maintain two queues.Our first queue will be our generated linked list and the second queue will hold the addition of two nodes, this will be our interal node with first dequeued node as left child and second dequeued node as right child
1. Dequeue two nodes from first queue, create a internal node with frequency equal to sum of two nodes frequencies and add that internal node to the second queue.
2. Now dequeue two nodes with the minimum frequency by examining the front of both queues. Repeat following steps two times 
        1. If second queue is empty, dequeue from first queue. 
        2. If first queue is empty, dequeue from second queue. 
        3. Else, compare the front of two queues and dequeue the minimum. 
3. Repeat step two until only one node is present in any one of the queue, that will be our root node.

while executing the code it takes the three command line arguments:
  1.  The name of file, in which data to be compressed is present
  2.  The name of file, in which codes to be stored
  3.  The name of file, in which decoded data to be stored
