Homework 4 Questions

Part A: Big-O table

Method           Structures it touches           Big-O             One-line reason

addSong          Doubly linked list              O(n)              It searches the entire playlist to make sure the ID is not already used, so it's O(n).

findSong         Doubly linked list              O(n)              It may have to search through every node to find the ID, so it's O(n).

play             Doubly linked list              O(n)              It searches the playlist for the requested song, so it's O(n).

queueLater       Doubly linked list              O(n)              findSong() takes O(n), while addLast() is O(1).
                 Deque

queueNext        Doubly linked list              O(n)              findSong() takes O(n), while addFirst() is O(1).
                 Deque

next             Doubly linked list              O(n)              Playing a queued or next song requires play(), which takes O(n).
                 Deque
                 Stack

back             Doubly linked list              O(n)              pop() is O(1), but queueNext() and play() each require a list search, which takes O(n).
                 Deque
                 Stack

removeSong       Doubly linked list              O(n)              It searches the playlist and may also search the queue, so it's O(n).
                 Deque

showPlaylist     Doubly linked list              O(n)              It visits every song in the playlist, so it's O(n).


Part B: Defend two choices
Pick two of your five structures. For each, write 3 to 5 sentences that answer:
• What job does it do in the player?
• What would get slower or harder if you swapped it for a plain array?
• If you reused a built-in, what does it cost compared with building your own?

Deque
• I used a deque to manage the songs that are queued to play next because I need to add songs to both the front and back. queueNext() uses addFirst() and queueLater() uses addLast(), so both operations are O(1) once the song is found. 

• Using a plain array would make adding to the front harder because existing elements would have to be shifted.

• I used Java's built-in ArrayDeque instead of building my own because it already provides efficient operations for both ends and saves me from implementing those operations myself.

Hash Map
• I used a HashMap for the library because each song has a unique ID that I can use as a key to quickly find the song. Adding, finding, and removing a song are O(1) on average, which is much faster than searching through the playlist with a linked list.

• If I used a plain array, I would have to search through the array to find a song, so it would be slower.

• I used Java's built-in HashMap because it already handles the hashing and storage for me instead of requiring me to implement a hash table from scratch.








