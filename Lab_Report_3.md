Bugs and Commands
=================
Failure-inducing input
----------------------
```
  @Test
  public void testReversedVer1(){
    int [] input = {1, 2, 3};
    assertArrayEquals(new int[]{3,2,1}, ArrayExamples.reversed(input));
  }
```

None failure-inducing input
---------------------------
```
  @Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
```

***
The symptoms
------------
![Image](ErrorTest.png)
![Image](ErrorTest2.png)

***

Before
------
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```

After
-----
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
  }
```
JUnit says that the first element in the returned array when ArrayExamples called revered method with input as the argument is different from the expected value. The value is expected to be 3 but the actual value in the 0 index of the newArray is actually {0, 0, 0}. The statement inside the for loop needs to be changed. Instead of assigning the element in newArray to arr and then returning arr, we want to assign values in arr to  newArray, then simply return newArray.

