graph TD
    A[开始] --> B[输入tasks, workers, pills, strength]
    B --> C[对tasks和workers进行排序]
    C --> D[初始化二分查找的左右边界 left = 1, right = min(m, n)]
    D --> E[while循环 left <= right]
    E --> F[计算中间值 mid = (left + right) / 2]
    F --> G[调用check函数 check(mid)]
    G --> H{check返回true?}
    H -->|是| I[更新ans = mid, left = mid + 1]
    H -->|否| J[更新right = mid - 1]
    I -->|继续| E
    J -->|继续| E
    E --> K[while循环结束]
    K --> L[返回ans作为最多可以完成的任务数]
    L --> M[结束]
