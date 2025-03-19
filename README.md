# DHeap
More stable and modern alternative to D's BinaryHeap, with small performance trade-offs.

```d
import DHeap.Heap;

Heap!int heap = Heap!int([1, 3, 2, 4, 6, 5, 7, 9, 8, 10], HeapType.MIN_HEAP); // MinHeap initialized. Values are automatically heapified.

heap.HeapPush(0); // Push zero to the heap. Automatically sifts the heap.
heap.HeapFront(); // Get heap front object. Returns zero as long as we have MIN_HEAP as a heap type.
heap.HeapPop(); // Pop the front object of the heap. Returns the front object before popping the object. Returns 0.
heap.Empty(); // Or heap.Empty (works as a @property). Check is the heap empty.
heap.Size(); // Or heap.Size (works as a @property). Get the heap size/length.

// Iterable via foreach!
foreach(int num; heap) { /** Some work to do... */ }
```
