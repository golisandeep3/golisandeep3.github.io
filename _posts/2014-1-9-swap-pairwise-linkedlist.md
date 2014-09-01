---
layout: post
title: Swap pairwise elements in a LinkedList
---


We can swap pairwise elements either by swapping data or by changing links.Below is the code implemented by changing links.

class Node
{
    int data;
    Node next;
}

public void pairwiselinks()
    {
        if(head==null)
        return;
        if(head.next==null)
        return;
        Node prev =head;
        Node curr = head.next;
        head= curr;
        
        while(true)
        {
            Node temp = curr.next;
            curr.next = prev;
            if(temp==null||temp.next==null)
            {
                prev.next = temp;
            break;
            }
            prev.next = temp.next;
            curr=temp.next;
            prev  = temp;
        }
    
    }
