# Lab Report 2 

## Part 1

1. A failure-inducing input for `reversed()`
```
@Test 
public void testReversed1() {
    int[] input1 = { 1, 2, 3, 4 };
    assertArrayEquals(new int[]{4, 3, 2, 1}, ArrayExamples.reversed(input1));
}
```

2. An input that doesn’t induce a failure for `reversed()`
```
@Test
    public void testReversed() {
    int[] input1 = { 0};
    assertArrayEquals(new int[]{ 0}, ArrayExamples.reversed(input1));
}
```

3. The symptom
![3a](./images/3a.png)

4. The bug

    - The code before 
    ```
    static int[] reversed(int[] arr) {
        int[] newArray = new int[arr.length];
        for(int i = 0; i < arr.length; i += 1) {
            arr[i] = newArray[arr.length - i - 1];
        }
        return arr;
    }
    ```
    - The code after 
    
    The code below fixes the error by fixing the LValue and RValue of the assignment statemtn in the for loop. The array being referenced on the right hand side should be the array that is passed as a parameter (`arr`), instead of the array that has been newly created (`newArray`). Additionaly, the array being mutated should be the newly created array (`newArray`). Finally, the array being returned should be the newly reversed array, instead of the same array that was passed to the function. 
    ```
    static int[] reversed(int[] arr) {
        int[] newArray = new int[arr.length];
        for(int i = 0; i < arr.length; i += 1) {
            newArray[i] = arr[arr.length - i - 1];
        }
    return newArray;
    }
    ```


## Part 2 

### The `find` command 
#### Alternate options for using `find`
1. 
    - On a file 
    - On a directory 
2. 
    - On a file 
    - On a directory
3. 
    - On a file 
    - On a directory
4. 
    - On a file 
    - On a directory


