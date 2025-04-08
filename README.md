# Sort-work（四種排序法）

本專案介紹四種常見的排序演算法：Insertion Sort、Quick Sort、Merge Sort 以及 Heap Sort，說明其原理、優缺點與適用場景。

---

## 📌 Insertion Sort（插入排序）

**原理：**  
插入排序的核心概念是「從未排序的資料中，挑出一個元素，插入到已排序的部分中」。  
想像打撲克牌時，把新牌插入到正確的位置中，讓手上的牌保持有序。

**操作方式：**
- 從第二個元素開始，向左比對，找到合適位置插入。
- 重複此動作直到陣列排序完成。

:heavy_check_mark: **優點：**
- 實作簡單、易懂。
- 適合資料量小或幾乎已排序的情況。
- 穩定排序（不改變相同值的相對順序）。
- 不需要額外記憶體（就地排序）。

:x: **缺點：**
- 最壞情況時間複雜度為 O(n²)，不適合大筆資料。
- 插入時可能需要大量元素移動，效率低。

---

## ⚡ Quick Sort（快速排序）

**原理：**  
使用「分治法」的概念，挑選一個基準值（pivot），將資料分為小於與大於它的兩邊，然後對左右遞迴排序。

**操作方式：**
1. 選定 pivot。
2. 將資料分成兩邊。
3. 對兩邊遞迴執行 Quick Sort。

:heavy_check_mark: **優點：**
- 平均效率高，時間複雜度為 O(n log n)。
- 就地排序，記憶體效率好。
- 實務中使用非常廣泛。

:x: **缺點：**
- 最壞情況時間複雜度為 O(n²)（選到最差 pivot 時）。
- 遞迴過深可能造成堆疊溢位。
- 不穩定排序（可能改變相同值的順序）。

---

## 🌀 Merge Sort（合併排序）

**原理：**  
使用「分治法」將資料不斷對半分，直到分成單一元素，再兩兩合併排序，直到重組回整體。

**操作方式：**
1. 將資料對半分割。
2. 遞迴排序左右兩部分。
3. 合併兩部分為排序結果。

:heavy_check_mark: **優點：**
- 穩定排序。
- 時間複雜度穩定為 O(n log n)。
- 適合處理大量資料，尤其是串流或外部排序。

:x: **缺點：**
- 空間需求大，需額外 O(n) 記憶體。
- 效率通常不如 Quick Sort。

---

## 🏗️ Heap Sort（堆積排序）

**原理：**  
利用最大堆（Max Heap）或最小堆的資料結構，維持每次取出最大值（或最小值）後重新調整堆來排序。

**操作方式：**
1. 將資料建成一個最大堆。
2. 每次取出堆頂元素放到結果末端。
3. 調整剩餘資料成最大堆，重複直到完成。

:heavy_check_mark: **優點：**
- 時間複雜度穩定為 O(n log n)。
- 不需要大量額外記憶體（就地排序）。
- 適合需要最壞情況效率穩定的場景。

:x: **缺點：**
- 不是穩定排序。
- 常數時間較大，實務效能通常略輸 Quick Sort。
- 程式實作較複雜。

---



