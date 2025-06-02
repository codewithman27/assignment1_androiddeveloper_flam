# assignment1_androiddeveloper_flam
# solution_1
# Overview
This is a Java implementation of a Least Recently Used (LRU) cache using a combination of a doubly-linked list and a hash map. The LRU cache evicts the least recently used items when it reaches its capacity limit.

## Features
O(1) average time complexity for both get and put operations

Fixed capacity that can be set during initialization

Automatic eviction of least recently used items when capacity is reached

Maintains access order to prioritize recently used items

## Implementation Details
Data Structures
Doubly-Linked List:

Maintains the order of items based on recent usage

Most recently used items are at the head

Least recently used items are at the tail

Nodes contain key, value, and pointers to previous/next nodes

HashMap:

Provides O(1) access to cache items by key

Maps keys to their corresponding nodes in the linked list
## Key Methods
LRUCache(int capacity):

Constructor that initializes the cache with a specific capacity

int get(int key):

Returns the value for the given key if it exists

Moves the accessed item to the head of the list (most recently used)

Returns -1 if key doesn't exist

void put(int key, int value):

Updates the value if the key already exists

Adds new key-value pair if key doesn't exist

Evicts the least recently used item if capacity is reached

Moves updated/added items to the head of the list

## Helper Methods:

addNode(Node newnode): Adds a new node right after the head

deleteNode(Node delnode): Removes a node from the linked list


**Performance**
Time Complexity:

1. get: O(1)

2. put: O(1)

Space Complexity: O(capacity)

# solution_2
## Overview
A simple hash map implementation in Java using chaining (linked lists) for collision resolution.

## Features
Basic hash map operations: put, get, and remove

Fixed size of 1000 buckets

Chaining with linked lists to handle collisions

Returns -1 for keys not found

Implementation Details
Hash Function: Simple modulo operation (key % 1000)

Data Structure: Array of linked lists (each bucket is a linked list)

Collision Handling: New entries are appended to the bucket's linked list

Usage Example
java
MyHashMap map = new MyHashMap();
map.put(1, 100);
map.put(2, 200);
System.out.println(map.get(1));  // 100
map.remove(2);
System.out.println(map.get(2));  // -1


# solution_3_Book Review App MVP

A minimal Android book review application built with Java using MVVM architecture, featuring offline capabilities with Room persistence.

## Features

- **Book Browsing**: View a list of books with titles, authors, and thumbnails
- **Detailed View**: See complete book details including description and rating
- **Favorites System**: Save books for offline access
- **Offline Mode**: Access saved books without internet connection
- **Mock API**: Integrated fake API service for development

## Tech Stack

- **Language**: Java
- **Architecture**: MVVM (Model-View-ViewModel)
- **Libraries**:
  - Android Jetpack (ViewModel, LiveData, Room)
  - Retrofit for networking
- **Persistence**: Room Database
- **Image Handling**: Custom placeholder system

## Project Structure



## Setup Instructions

### Prerequisites

- Android Studio (latest version)
- Android SDK (API 28+)
- Java JDK 11+

### Installation

1. Open the project in Android Studio

2. Sync Gradle dependencies

3. Build and run the app
