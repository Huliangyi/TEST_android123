

| 操作          | 耗时                                                         |
| ------------- | ------------------------------------------------------------ |
| Scatter       | $(p-1)(\alpha+\frac np\beta)=(p-1)\alpha+\frac {p-1}p n\beta$  |
| Gather        | $ (p-1)(\alpha+\frac np\beta)=(p-1)\alpha+\frac {p-1}p n\beta $     |
| Broadcast     | $ (p-1)(\alpha+n\beta)=(p-1)\alpha+ (p-1)n\beta $    |
| Reduce     | $ (p-1)(\alpha+n\beta + n\gamma)=(p-1)\alpha+ (p-1)n\beta +(p-1)n\gamma$                                        |
|  ReduceScatter |  $ (p-1)(\alpha+\frac{n}{p}\beta+\frac{n}{p}\gamma)=(p-1)\alpha+\frac{p-1}{p}n\beta+\frac{p-1}{p}n\gamma $  |
|  AllGather    | $ (p-1)(\alpha+\frac{n}{p}\beta)=(p-1)\alpha+\frac{p-1}{p}n\beta $  |
| AllReduce     | 实现为ReduceScatter +  Allgather: <br> $ 2(p-1)\alpha+2\frac{p-1}{p}n\beta+\frac{p-1}{p}n\gamma $ |



