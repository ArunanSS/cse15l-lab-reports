# Lab Report 3
## **Arunachalam Senthil**

Bug Chosen: averageWithoutLowest

## Failure inducing Input

```java
public void testAverageWithoutLowest() {
    int[] numbers = {5, 2, 7, 3, 8};
    assertEquals(4.75, ArrayMethods.averageWithoutLowest(numbers), 0.001);
}
```

## Doesn't Induce a Failure
```java
public void testAverageWithoutLowestNoChange() {
    int[] numbers = {2, 4, 6, 8, 10};
    assertEquals(6.0, ArrayMethods.averageWithoutLowest(numbers), 0.001);
}
```







