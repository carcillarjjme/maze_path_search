# Maze Path Search

A simple implementation of basic path search algorithms namely:
- Depth-First Search
- Breadth-First Search

The script reads from *maze.xlsx* for the maze. There are two sheets namely:
- maze_20by20
- maze_101by101

which differ on the maze sizes as name suggests. The maze input uses "#" as barrier blocks and "" (empty) cells as path blocks. Example:

| **Row**    | **A** | **B** | **C** | **D** | **E** | **F** | **G** | **H** | **I** |
|:----------:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
| **1**      |       |       |       |       |       |       |       |       |       |
| **2**      |       | #     | #     | #     |       | #     | #     | #     | #     |
| **3**      |       | #     | #     | #     |       | #     |       |       |       |
| **4**      |       |       |       |       | #     | #     | #     | #     | #     |
| **5**      | #     | #     | #     |       |       |       |       |       |       |
| **6**      |       | #     | #     |       | #     |       | #     |       | #     |
| **7**      |       | #     | #     |       | #     |       | #     |       | #     |
| **8**      |       | #     | #     |       | #     |       | #     |       | #     |
| **9**      |       |       |       |       | #     |       | #     |       | #     |
| **10**     | #     | #     | #     |       | #     |       | #     |


## Starting and Ending Nodes
Change the starting and ending nodes via these lines. Currently these are selected at random. The current setup loops over 5 pairs of starting and ending nodes.

```python
starts = np.random.choice(range(0,3500),5)
ends = np.random.choice(range(4000,5007),5)
```