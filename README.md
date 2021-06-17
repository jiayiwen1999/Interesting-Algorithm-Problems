# Interesting-Algorithm-Problems
A collection of some interesting algorithm problems that I have encountered so far.
1. Find all duplicates in an array
    Given an array with length n and the elements of the array are in the range of 1 to n. Return an array with all duplicates with no extra space and within O(n) time. 
    The idea is to encode the array as a hashmap, we can do so since the elements range from 1 to n. Thus, for any number i in [n], we can relate that to the status of array[i]. This gives us a hashmap structure. Also, we can work in modulo n. So in practice, we iterate over the array, then we relate the i th element in  the array with the arr[i] mod n th element in the original array. If the value of arr[ arr[i] % n ] is less or equal to n, then we haven't encounter this element before. To record this visit, we add n to this number. 
    Then we iterate over the array again to create the result array. If some elements has added n more than twice, we put them into the result. 
