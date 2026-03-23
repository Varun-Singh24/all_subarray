# Print All Subarrays of an Array (C++)

This repository contains a C++ implementation that generates and prints all possible contiguous subarrays from a given integer array.

---

## 🚀 How the Algorithm Works

The program uses **three nested loops** to define and print subarrays:

1.  **Outer Loop (`st`):** Determines the starting index of the subarray.
2.  **Middle Loop (`end`):** Determines the ending index of the subarray (starting from `st`).
3.  **Inner Loop (`i`):** Iterates from `st` to `end` to print the elements belonging to that specific subarray.

## 📊 Complexity Analysis

| Metric | Complexity | Description |
| :--- | :--- | :--- |
| **Time Complexity** | $O(n^3)$ | We have three nested loops. For an array of size $n$, the total operations are roughly $\sum_{st=0}^{n-1} \sum_{end=st}^{n-1} (end - st + 1)$, which simplifies to cubic time. |
| **Space Complexity** | $O(1)$ | The program does not use any extra space that scales with input size; it prints directly to the console. |

---

## 💻 Code Overview

The logic uses standard loops and indexing:

```cpp
for (int st = 0 ; st < n ; st++) {
    for (int end = st; end < n ; end++ ) {
        for(int i = st; i <= end ; i++ ) {
            cout << arr[i]; 
        }
        cout << " "; 
    }
    cout << endl; 
}
```

📝 Example Output
For an array {1, 2, 3, 4, 5}:
O/P 
```
1 12 123 1234 12345 
2 23 234 2345 
3 34 345 
4 45 
5 
```
