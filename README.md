# CSC212Lists
List Data Structures via Testing 

### ListADT Methods to implement

```java
public abstract class ListADT<T> ... {
  ...
  
  public T removeFront();
  public T removeBack();
  public T removeIndex(int index);
  
  public void addFront(T item);
  public void addBack(T item);
  public void addIndex(int index, T item);

  public T getFront();
  public T getBack();
  public T getIndex(int index);
  
  public void setIndex(int index, T value);

  public int size();
  public boolean isEmpty();
}
```

### Errors:

Where appropriate, you should throw my error classes instead of ``NullPointerException``s or ``ArrayIndexOutOfBoundsException``s. It is good programming practice to not expose those to your users, and it also demonstrates that you're reasoning about your code and its failure cases.

I provide errors for:
- ``TODOErr``, so I can quickly tell if you have not changed the starter code in a particular case. You will be deleting these errors, not adding them.
- ``EmptyListError``, when a remove or get operation is called on an empty list. See ``checkNotEmpty()``
- ``BadIndexError``, when a getIndex, addIndex or removeIndex operation is called with an index that does not exist. See ``checkExclusiveIndex`` and ``checkInclusiveIndex``.
- ``RanOutOfSpaceError``, when an add method fails on a ``FixedSizeList`` because it has run out of space.

Prefer the most precise error: ``EmptyListError`` rather than a ``BadIndexError`` when looking for the 5th thing in an empty list.

## Rubric (100)

Right now, when I run all the tests in this project, I get the following output:

    
Tests run: 142, Failures: 0, Errors: 90, Skipped: 0

So there are 52 passing tests, and 90 failing tests.

Your score on this assignment will range up to 100 -- the fraction of the tests that pass on your code (minus the tests that already pass), provided:

 1. there are no code compilation problems with your code (red lines or Problems in Eclipse).  
 2. you do not rename any methods or modify the tests in any way, and 
 3. you resolve any infinite loops in your code (better to comment out that method and have it crash than run forever -- it prevents other tests from running.

## What should I do first?

There are TODOErr methods in:

Start with ``FixedSizeList``.
- (2) src/main/java/edu/smith/cs/csc212/adtr/real/FixedSizeList.java

Then, work to complete ``GrowableList`` which is an ArrayList implementation based on ``FixedSizeList`` but it needs a resizeArray method to be completed.
- (4) src/main/java/edu/smith/cs/csc212/adtr/real/GrowableList.java

Then, work on ``SinglyLinkedList``: This will be very hard if you are unwilling to draw pictures.
- (9) src/main/java/edu/smith/cs/csc212/adtr/real/SinglyLinkedList.java

Then, work on ``DoublyLinkedList``: Some methods will be just like SinglyLinkedList (front methods) and some will be very different.
- (12) src/main/java/edu/smith/cs/csc212/adtr/real/DoublyLinkedList.java

Then, work on ``ChunkyArrayList``: This data structure is very different from the others, because it uses GrowableList and FixedSizeList to make another.
- (9) src/main/java/edu/smith/cs/csc212/adtr/real/ChunkyArrayList.java



