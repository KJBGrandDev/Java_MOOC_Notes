### Learning objectives

- You know what an Array is and how to use it.
- You can create an Array, assign a value to a given index and iterate over it.
- You recognize that an Array is a reference type and know how to use an array as a parameter of a method

We've gotten familiar with the ArrayList, which has a lot of functionality to make the life of a programmer easier. Perhaps the most important is about adding elements. From the point of view of the programmer, the size of the ArrayList is unlimited. In reality there are no magic tricks in the ArrayList — they have been programmed like any other programs or tools offered by the programming language. When you create a list, a limited space is reserved in the memory of the computer. When the ArrayList runs out of space, a larger space is reserved and the data from the previous space is copied to the new one.

Even though the ArrayList is simple to use, sometimes we need the ancestor of the ArrayList, the Array.

An Array contains a limited amount of numbered spots (indices) for values. The length (or size) of an Array is the amount of these spots, i.e. how many values can you place in the Array. The values in an Array are called **elements**.