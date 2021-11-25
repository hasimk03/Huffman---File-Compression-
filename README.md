# Huffman---File-Compression-
Respository contains folders and files that implement a file compression program, based on Huffman coding. 

Respository contans multiple classes that are all used in conjunction with the main file HuffmanCoding
The details are given below:

CharFreq: This class creates a new object called CharFreq, which contains a Char value 'character' and a double value 'probOcc'. The charFreq object is used to track and determine the probability that specific char appears in a defined input file.

Queue: This class implements a queue of generic type, this is the main data structure that will be used in the HuffmanCoding file

TreeNode: This class implements a LinkedList using TreeNodes, as its node. Each node contains a reference to its next and previous nodes, as well as a charFreq object stored in its data. This doubly LinkedList will be used to implement the queue.

HuffmanCoding: This class is the main project file which will refer to all other classes in order to implement the Huffman coding Algorithim.
The file takes a input file from the user, encodes itfollowing the Huffman coding algorithim, and finally takes this file and decodes it back into the original file. The methods are given below:

  makeSortedList -> reads an input file, one char at a time, and creates an ArrayList of charFreq objects, where each object contains a reference to a set    character, and the probability of its occurence in the input file

  makeTree() -> Takes in the file from makeSortedList() and creates a Huffman Coding tree, where the absolute children represent charFreq objects, and the parents  represent the sum of children. The root of the tree returns 1.00

  makeEncodings() -> grabs the output of makeSortedList(), traverses the tree and stores 0 and 1's for left and right traversals of the tree. The method then creates unique encodings (containing a string of 0's and 1's), where each encoding corresponds to each charFreq object

  encodeFromArray() -> Reads through the input file, and uses the encodings created in the previous method, to overwrite the existing byte to the encoding previously found.

  decode() -> takes the encoded file, and uses the previous methods to convert the encoded file back to the orignal.

The program follows a methodology to create a new encoded file (equivalent to input file), where the encoded file size is much smaller than the input file.

StdIn and StdOut are classes used to read inputs from the command line, and output to it



All methods detailed above were implemented by myself, where the general framework was created by university instructors. This project was submitted as apart of school assignment.


