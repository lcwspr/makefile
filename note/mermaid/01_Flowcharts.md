# FlowChart

- [FlowChart](#flowchart)
  - [节点定义](#节点定义)
    - [Graph](#graph)
  - [节点形状](#节点形状)

- 所有的流程图都是由节点,几何图形,边线，箭头和线组成的组成的(node), Mermaid代码定义了节点和边线被创建和交互的方式, 同时也提供了不同的箭头类型，多方向箭头以及和子图之间的连接

- 不要使用关键字end等作为流程图节点，end的大小写任何形式都会导致流程图中断

## 节点定义

1. 一个节点(default)

    - 语法

        ```text
        flowchart LR
            id
        ```

    - show

        ```mermaid
        flowchart LR
            id
        ```

2. 一个带有文本的节点

    - 可以在盒子中设置和id值不同的文本，如果多次这样做，节点上最后出现的文本会被使用，同样的，如果之后你对于节点定义了边界，那么能够省略文本定义，当渲染盒子时候，前一个定义将会被使用

    - 语法

        ```text
        flowchart LR
            id1[This is the text in the box]
        ```

    - show

        ```mermaid
        flowchart LR
            id[This is the text in the box]
        ```

### Graph

- 可以声明流程图的方式是从上到下的(TD / TB)

  - 语法

    ```text
    flowchart TB
        start ---> Stop
    ```

  - show

    ```mermaid
    flowchart TB
        Start --> Stop
    ```

- 流程图方向

  1. TB : top to bottom

  2. TD: top down

  3. BT: bottom to top

  4. RL: right to left

  5. LR: left to right

## 节点形状

1. 带有圆边的节点(a node with round edges)

    - 语法

      ```text
      flowchart LR
        id(This is text in the box)
      ```

    - show

      ```mermaid
      flowchart LR
        id(This is text in the box)
      ```

2. 体育场形节点(a stadium-shaped node)

    - 语法

      ```text
      flowchart LR
        id1([This is text in the box])
      ```

    - show

      ```mermaid
      flowchart LR
        id1([This is text in the box])
      ```

3. 子程序形状(a node in a subroutine shape)

    - 语法

      ```text
      flowchart LR
        id1[[This is text in the box]]
      ```

    - show

      ```mermaid
      flowchart LR
        id1[[This is text in the box]]
      ```

4. 圆柱形

    - 语法

      ```text
      flowchart LR
        id1[(DateBase)]
      ```

    - show

      ```mermaid
      flowchart LR
        id1[(DateBase)]
      ```

5. 圆形节点

    - 语法

      ```text
      flowchart LR
        id1>This is text in the box
      ```

    - show

      ```mermaid
      flowchart LR
        id1((This is text in the box))
      ```

6. 不对称节点

    - 语法

      ```text
      flowchart LR
        id1>This is text in the box]
      ```

    - show

      ```mermaid
      flowchart LR
        id1>This is text in the box]
      ```