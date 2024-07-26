
class Solution {
    public ListNode reverseList(ListNode head) {
        return reverse(head,null);
    }
    private ListNode reverse(ListNode curr, ListNode prev){
        if(curr == null){
            return prev;
        }
        ListNode temp = reverse(curr.next, curr);
        curr.next = prev;
        return temp;
    }   
    }
