# Sort-work（四種排序法）

本專案介紹四種常見的排序演算法：Insertion Sort、Quick Sort、Merge Sort 以及 Heap Sort。說明其原理、優缺點、適用情境，並探討在不使用其他排序法的情況下如何改善缺點。

---

## 📌 Insertion Sort（插入排序）

**原理：**  
每次從未排序區域中選取一個元素，插入到已排序區域中的正確位置。

🟢 **優點：**
- 實作簡單、容易理解。
- 資料量小或接近排序時效率不錯。
- 穩定排序（相同元素順序不變）。
- 就地排序，不需額外空間。

🔴 **缺點：**
- 時間複雜度 O(n²)，不適合大筆資料。
- 每次插入可能造成大量資料移動。

🔧 **改善方式：**
- 使用 **Binary Search** 找插入點，減少比較次數。
- 減少 swap 次數，使用暫存變數搬移資料。
- 若資料接近排序，加入中止條件加快效率。

---

## ⚡ Quick Sort（快速排序）

**原理：**  
挑選一個 pivot，將陣列分為小於與大於 pivot 的兩部分，分別遞迴排序。

🟢 **優點：**
- 平均效率高，O(n log n)。
- 記憶體效率好（就地排序）。
- 實務中廣泛使用。

🔴 **缺點：**
- 最壞情況為 O(n²)，例如資料已排序。
- 遞迴過深可能導致 stack overflow。
- 不穩定排序。

🔧 **改善方式：**
- 使用 **隨機 pivot** 或 **三數取中法**，降低最壞情況發生機率。
- 遞迴優化（尾遞迴 → 迴圈），降低堆疊深度。
- 對小區段提早終止遞迴，提高效率。

---

## 🌀 Merge Sort（合併排序）

**原理：**  
使用分治法將陣列不斷切半排序，最後進行合併。

🟢 **優點：**
- 穩定排序。
- 時間複雜度穩定 O(n log n)。
- 適合大型資料與外部排序。

🔴 **缺點：**
- 空間需求高，需要 O(n) 額外記憶體。
- 常數時間開銷大，實務表現略低於 Quick Sort。

🔧 **改善方式：**
- 使用 **Bottom-up 合併**，改為迴圈實作，省堆疊。
- 合併時先檢查是否已排序（直接跳過）。
- 重複利用暫存陣列，減少記憶體分配次數。

---

## 🏗️ Heap Sort（堆積排序）

**原理：**  
使用最大堆資料結構，每次將堆頂（最大）與末尾交換後重新堆積。

🟢 **優點：**
- 時間複雜度穩定 O(n log n)。
- 記憶體需求低。
- 最壞情況效率穩定。

🔴 **缺點：**
- 不穩定排序。
- 常數時間開銷大，效能略差於 Quick Sort。
- 較難實作。

🔧 **改善方式：**
- 使用 **Bottom-up Heapify** 建堆，建堆只需 O(n)。
- 減少 swap，用暫存變數替代交換。

---
