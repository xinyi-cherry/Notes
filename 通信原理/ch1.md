# 第一章

## 通信系统模型

- 通信系统一般模型
```mermaid
flowchart LR
    id1(信源)
    id2(发送设备)
    id3(信道)
    id4(接收设备)
    id5(信宿)
    id6(噪声源)
    subgraph signal
    id1--发送端-->id2-->id3-->id4--接收端-->id5
    end
    subgraph noise
    id6-->signal
    end
```

- 模拟通信系统模型
```mermaid
flowchart LR
    id1(模拟信源)
    id2(调制器)
    id3(信道)
    id4(解调器)
    id5(信宿)
    id6(噪声源)
    subgraph signal
    id1-->id2-->id3-->id4-->id5
    end
    subgraph noise
    id6-->signal
    end
```
## 信息及其度量

- 信息量
设 $P(x)$ 表示消息发生的概率， $I$ 表示消息中所含的信息量，则有以下关系：

$$ I = log_a\frac{1}{P(x)} = -log_aP(x) $$

$ a $ 的取值不同，信息量的单位也不同，下表是取值与单位之间的关系


| $ a $ | 单位 |
| :---: | :-------: |
|   2   | b(比特) |
| $ e $ | nat(奈特) |
|  10   | Hartley(哈特莱) |

- 信息熵

$$ H(x) = -\sum_{i=1}^{M}P(x_i)log_2P(x_i)\ \ (b/符号)$$