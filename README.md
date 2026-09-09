# Leetcode-problem-234--Palindrome-Linked-List-
Solution for problem 234 on leetcode 

 ## Approach

The code uses a **stack** to check whether the linked list is a palindrome.

* Traverse the entire linked list and push every node's value into a stack.
* Traverse the linked list again from the beginning.
* Compare each node's value with the value at the **top of the stack**.
* If any values differ → return `false`.
* If all values match → return `true`.
* Since a stack returns elements in reverse order, this effectively compares the list with its reverse.

## Algorithm

1. Create an empty stack `Stk`.
2. Set `temp = head`.
3. Traverse the linked list:

   * Push `temp->val` into the stack.
   * Move `temp` to the next node.
4. Reset `temp = head`.
5. Traverse the linked list again:

   * Compare `temp->val` with `Stk.top()`.
   * If they are different, return `false`.
   * Otherwise, pop the stack and move to the next node.
6. If the complete list is checked without mismatch, return `true`.

## Complexity

Let **n = number of nodes**.

* **Time Complexity:** `O(n)`

  * First traversal: `O(n)`
  * Second traversal: `O(n)`
  * Overall: `O(n)`

* **Space Complexity:** `O(n)`

  * The stack stores all `n` node values.

**Final:**
**Time = O(n)**
**Space = O(n)**
