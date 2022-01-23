---
tags: algorithm linked-list
---

# 链表

## 算法题

### 回文链表

* #递归 （#后续遍历)，相当于调用栈，递归时候把链值入栈
* 把首节点保存
* 递归压栈，到最后节点时开始比对左右节点

```typescript
/**
 * Definition for singly-linked list.
 * class ListNode {
 *     val: number
 *     next: ListNode | null
 *     constructor(val?: number, next?: ListNode | null) {
 *         this.val = (val===undefined ? 0 : val)
 *         this.next = (next===undefined ? null : next)
 *     }
 * }
 */

function isPalindrome(head: ListNode | null): boolean {
    let left = head

    const traverse = (right: ListNode | null) => {
        if (!right) return true
        // 压栈
        let res = traverse(right.next)

        res = res && right.val === left.val
        left = left.next
        return res
    }

    return traverse(head)
}
```

