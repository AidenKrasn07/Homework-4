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

back             Doubly linked list              O(n)              pop() is O(1), but queueNext() and play() each require a list search, which takes O(n).
                 Deque

removeSong       Doubly linked list              O(n)              It searches the playlist and may also search the queue, so it's O(n).
                 Deque

showPlaylist     Doubly linked list              O(n)              It visits every song in the playlist, so it's O(n).


Part B: Defend two choices
Pick two of your five structures. For each, write 3 to 5 sentences that answer:
• What job does it do in the player?
• What would get slower or harder if you swapped it for a plain array?
• If you reused a built-in, what does it cost compared with building your own?
