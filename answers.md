# CMPS 2200 Assignment 5
## Answers

**Name:**_Reid Miller_


- **1a.**
$ceil(log_d{|E|})$

- **1b.**
delete-min: $O(dlog_d{|E|})$, insert: $O(log_d{|E|})$

- **1c.**
$O(|E|log_d{|E|})$

- **1d.**
Given our work found in 1c, the only way to make $O(|E|log_d{|E|})=O(|E|)$ is by making $log_d{|E|}=1$. The value of d that makes this expression true is $d=|E|$. This results in $O(|E|log_{|E|}(|E|))=O(|E|)$

- **2a.**
$APSP(0, 1, 2)=-2$
$APSP(0, 2, 2)=-1$
$APSP(1, 2, 2)=0$

$APSP(0, 1, 1)=-2$
$APSP(0, 2, 1)=-1$
$APSP(1, 2, 1)=0$

$APSP(0, 1, 0)=-2$
$APSP(0, 2, 0)=2$
$APSP(1, 2, 0)=1$

- **2b.**
Yes there is a relationship. In this specific graph, these values would be the same. This is because you can only visit each node once. Since there are 3 nodes in this graph, you can visit all three when $k=1$ or when $k=2$. For any value of $k>=n-2$, every $APSP(i, j, k)$ would be equivalent.

Yes, since $APSP(i, j, 1)$ is equal to $APSP(i, j, 2)$ in this graph, you could just write $APSP(i, j, 1)$ and get the same value.

- **2c.**
$APSP(i, j, k)=min(APSP(i, j, k-1), APSP(i, k, k-1) + APSP(k, j, k-1))$

- **2d.**
Given the total number of subproblems is $n^2*(n-1)$ and the work per subproblem is $n^2$, the total work would be $O(n^5)$

- **2e.**
Since the work of Johnson's Algorithm is $O(|V|*|E|log|E|)$. As a result, our algorithm would be worse at all values.

- **3a.**
No. MST minimizes the total edge weight while MMET might forego the option which minimizes total edge weight in favor of choosing the shortest edge immediately available.

- **3b.**
Let's say our MST has n edges. To find the 2nd best option, we would find the MST if we were not allowed to use edge 1. Then we would do this again, but without using edge 2. We would do this repeatedly until we reach edge n. Now, we have every optimal MST except for the most efficient. We could then compare these values, and choose the one with the smallest weights.

- **3c.**
$O(n*|E|log|E|)$ where n is the number of edges in our original MST.
