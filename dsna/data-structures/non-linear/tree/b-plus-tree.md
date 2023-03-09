# :heavy_check_mark: B+ Tree
*Last Updated: 1/25/2023*

## :round_pushpin: Summary
- Downside of B-Tree is that it stores data pointer (pointer to disk file containing key value) and key value in the node of a B-Tree.
  - This reduces number of entries that can be packed into a node of a B-Tree.
  - Contributes to increase in number of levels in the B-Tree.
  - Increases search time of a record.
- B+ Tree eliminates this downside.
  - Stores data pointers only at the leaf nodes.
  - Leaf nodes must store all key values along with their corresponding data pointers to disk file block.
- Leaf nodes form first level of index.
- Internal nodes form other levels of multilevel index.

## :round_pushpin: Properties
- ***Review later***
