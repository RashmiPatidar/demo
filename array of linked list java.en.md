+++
title = "Array of Linked List in Java"
date = 2021-06-23
draft = false
description = "This article introduces array of linked list in Java."
keywords = ["Array of linked list Java "]
inarticle = true
tags = ["Java", "Linked list"]
author = "Rashmi Patidar"
postlink = 20202889

+++

`LinkedList` is the sequential and linear data structure that stores elements in a defined order. The structure is a part of `Collection` interface and is present in `java.util` package. The linked list has elements stored in `node`. Each node has a `data` part that stores element, and the `pointer` to store the next location. The elements in the list are not stored in contiguous memory locations.

## Demonstrate the Linked List Array using traditional array

Below is the code block that creates an array of linked list using loops.

```java
import java.util.LinkedList;

public class ArrayOfLinkedList {
    public static void main(String[] args) {
        LinkedList[] list = new LinkedList[5];
        for (int i = 0; i < 5; i++) {
            if (list[i] == null) {
                list[i] = new LinkedList();
                int temp = i;
                for (int j = 0; j < temp + 1; j++) {
                    list[i].add(j);
                }
            }
            System.out.print(list[i]);
        }
    }
}
```

In the above code block, a linked list is prepared using `new LinkedList[5]` statement. The new keyword calls the public constructor of the class linked list. The value five demonstrates the size of the array. So the array of five linked list are created. Over the list variable the loop runs to instantiate a new linked list over each node.  So a for loop gets applied with a condition of integer value less than five starts running. Internally it checks the condition, if the node first that is `list[i]` is null, then it instantiates the node with a new Linked List. Then again a for loop is used to fill the elements in the list. The `add` method gets used to append the elements at the end of the list. The method is from `LinkedList` class, and returns the `boolean` value. It returns true is the add is successfully done, else returns false. Similarly iteration continues and the each node's value get filled with the linked list. And the same is printed inside the loop to check the values filled in the nodes. 

Below is the output for the same.      

```output
[0]
[0, 1]
[0, 1, 2]
[0, 1, 2, 3]
[0, 1, 2, 3, 4]
```

## Demonstrate the linked list array using the Java8 methods

