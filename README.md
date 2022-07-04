# CS201_project_lru_cache

ABSTRACT

In computing, cache algorithms (cache replacement algorithms or cache replacement policies) are optimizing instructions or algorithms that a computer program or a hardware-maintained structure can follow in order to manage a cache of information stored on the computer. When the cache is full, the algorithm must choose which items to discard to make room for the new ones. In This Project we Implements Cache Simulator using Least Recently Used LRU.

BACKGROUND

Least Recently Used (LRU) algorithm requires keeping track of what was used when, which is expensive if one wants to make sure the algorithm always discards the least recently used item. General implementations of this technique require keeping "age bits" for cache-lines and track the "Least Recently Used" cache-line based on age-bits. In such an implementation, every time a cache-line is used, the age of all other cache-lines changes. LRU is actually a family of caching algorithms with members including 2Q by Theodore Johnson and Dennis Shasha and LRU/K by Pat O'Neil, Betty O'Neil and Gerhard Weikum. Because of implementation costs, one may consider algorithms (like those that follow) that are similar to LRU, but which offer cheaper implementations. One important advantage of the LRU algorithm is that it is amenable to full statistical analysis. It has been proven, for example, that LRU can never result in more than N-times more page faults than OPT algorithm, where N is proportional to the number of pages in the managed pool. On the other hand, LRU's weakness is that its performance tends to degenerate under many quite common reference patterns. For example, if there are N pages in the LRU pool, an application executing a loop over array of N + 1 pages will cause a page fault on each and every access. As loops over large arrays are common, much effort has been put into modifying LRU to work better in such situations. Many of the proposed LRU modifications try to detect looping reference patterns and to switch into suitable replacement algorithm, like Most Recently Used (MRU). Variants on LRU

  1. LRU-K evicts the page whose K-th most recent access is furthest in the past. For example, LRU-1 is simply LRU whereas LRU-2 evicts pages according to the time of their penultimate access. LRU-K improves greatly on LRU with regards to locality in time.

  2. The ARC algorithm extends LRU by maintaining a history of recently evicted pages and uses this to change preference to recent or frequent access. It is particularly resistant to sequential scans.
