# Lab 6: Russian Dictionary in C++

## Assignment Translation

**Laboratory Work No. 6**  
Separate report, for grade 4 or 5.

1. For an arbitrary Russian text, build a dictionary based on **Red-Black Trees**.  
   Implement the following operations:
   - add a word
   - delete a word
   - search for a word

   It is forbidden to use ready-made data structures.

   Also implement:
   - full dictionary clearing
   - loading/extending the dictionary from a text file

2. For the same Russian text, implement a **Hash Table** that supports:
   - adding a word
   - deleting a word
   - searching for a word

   Based on this hash table, implement a dictionary.

   The hash function can be chosen freely, but it must not be trivial, for example, using only the first letter of the word is not allowed.

   In the report, describe the quality of the hash function and its resistance to collisions.

   Also implement:
   - full dictionary clearing
   - loading/extending the dictionary from a text file

## Project Description

This project implements two dictionary structures for Russian text in C++:

1. Dictionary based on a Red-Black Tree
2. Dictionary based on a custom Hash Table

The program allows adding, deleting, searching, clearing, and loading words from a text file.


## Main Features

- Work with Russian text
- Add words to the dictionary
- Delete words from the dictionary
- Search words in the dictionary
- Load words from a `.txt` file
- Clear the whole dictionary
- Compare two dictionary implementations:
  - Red-Black Tree
  - Hash Table

## Restrictions

Ready-made data structures such as the following are not used for the main implementation:

- `std::map`
- `std::set`
- `std::unordered_map`
- `std::unordered_set`

The Red-Black Tree and Hash Table are implemented manually.

## Hash Function

The hash table uses a non-trivial hash function, for example a polynomial rolling hash.

The idea is to process every character of the word and combine it with a multiplier:

```text
hash = hash * p + character_code
