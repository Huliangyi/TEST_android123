| 操作          | 写法 | 耗时                                                         |
| -------------| ------------- | ------------------------------------------------------------ |
| Scatter  |<span style="color:#66b966;">**正确写法**   </span>   | $(p-1)(\alpha+\frac np\beta)=(p-1)\alpha+\frac {p-1}p n\beta$  |
| Gather   |<span style="color:#e60000;">**错误写法**</span>      | $ (p-1)(\alpha+\frac np\beta)=(p-1)\alpha+\frac {p-1}p n\beta $     |
| Broadcast   |<span style="color:#66b966;">**正确写法** </span>  | $(p-1)(\alpha+n\beta)=(p-1)\alpha+ (p-1)n\beta$    |
| Reduce   |<span style="color:#e60000;">**错误写法**</span>   | $ (p-1)(\alpha+n\beta + n\gamma)=(p-1)\alpha+ (p-1)n\beta +(p-1)n\gamma$                                        |
|  ReduceScatter   |<span style="color:#66b966;">**正确写法**</span> |  $(p-1)(\alpha+\frac{n}{p}\beta+\frac{n}{p}\gamma)=(p-1)\alpha+\frac{p-1}{p}n\beta+\frac{p-1}{p}n\gamma$  |
|  AllGather   | <span style="color:#e60000;">**错误写法**</span> | $ (p-1)(\alpha+\frac{n}{p}\beta)=(p-1)\alpha+\frac{p-1}{p}n\beta $  |
| AllReduce    | <span style="color:#66b966;">**正确写法**</span> | 实现为ReduceScatter +  Allgather: <br> $2(p-1)\alpha+2\frac{p-1}{p}n\beta+\frac{p-1}{p}n\gamma$ |
