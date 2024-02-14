# Lab Report 3
## **Arunachalam Senthil**


### Part 1
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

##  Symptom, as the output of running the tests

<img width="1133" alt="Screenshot 2024-02-13 at 10 25 56 PM" src="https://github.com/ArunanSS/cse15l-lab-reports/assets/83483462/449e8611-5e59-44b8-8a98-50d84a384a2b">


## Before Fix

```java
public static double averageWithoutLowest(int[] numbers) {
    if (numbers.length < 2) {
        throw new IllegalArgumentException("Array length must be at least 2");
    }

    int lowest = numbers[0];
    int sum = 0;

    for (int number : numbers) {
        sum += number;

        if (number < lowest) {
            lowest = number;
        }
    }

    return (double) (sum - lowest) / (numbers.length - 1);
}
```

## After Fix

```java
public static double averageWithoutLowest(int[] numbers) {
    if (numbers.length < 2) {
        throw new IllegalArgumentException("Array length must be at least 2");
    }

    int sum = 0;

    for (int number : numbers) {
        sum += number;
    }

    int lowest = Arrays.stream(numbers).min().orElseThrow();

    return (double) (sum - lowest) / (numbers.length - 1);
}
```

## Brief Explanation
The method's lowest value calculation had a problemn initially. To solve this we can see that the least value in the array is found using the incorrect array issue, and this makes it into a better  computation without mdthe lowest value.



### Part 2

1. This is for finding files by name:

Command:
<img width="322" alt="Screenshot 2024-02-13 at 9 01 23 PM" src="https://github.com/ArunanSS/cse15l-lab-reports/assets/83483462/958f6924-6a6f-4de4-b3b9-cb751deef75b">

Output:
<img width="400" alt="Screenshot 2024-02-13 at 9 01 35 PM" src="https://github.com/ArunanSS/cse15l-lab-reports/assets/83483462/241bb262-2a36-4603-b370-7cb2dc343e0f">

Source: "https://www.redhat.com/sysadmin/linux-find-command"


2. Finding directories

Command:
<img width="264" alt="Screenshot 2024-02-13 at 9 02 47 PM" src="https://github.com/ArunanSS/cse15l-lab-reports/assets/83483462/89f72ee8-ec82-440b-ad3b-75912c7fdda7">

Output:
<img width="216" alt="Screenshot 2024-02-13 at 9 03 04 PM" src="https://github.com/ArunanSS/cse15l-lab-reports/assets/83483462/9d3f7657-efda-4909-8ec9-ee8ff2650b64">

Source: "https://www.cyberciti.biz/faq/howto-find-a-directory-linux-command/#:~:text=cards%20as%20follows%3A-,find%20%2F%20%2Dtype%20d%20%2Dname%20%22project.,type%20d%20%2Dname%20%22project."

3. This is for finding files based on size

Command:
<img width="333" alt="Screenshot 2024-02-13 at 9 03 55 PM" src="https://github.com/ArunanSS/cse15l-lab-reports/assets/83483462/df629d69-af2d-4d4c-a265-0af181904531">

Output:
<img width="322" alt="Screenshot 2024-02-13 at 9 04 25 PM" src="https://github.com/ArunanSS/cse15l-lab-reports/assets/83483462/d0f93744-2815-4934-91f0-3e53e26e12cb">

Source: "https://linuxconfig.org/how-to-use-find-command-to-search-for-files-based-on-file-size"

4. Finding files modified within days

Command: 
<img width="403" alt="Screenshot 2024-02-13 at 9 04 56 PM" src="https://github.com/ArunanSS/cse15l-lab-reports/assets/83483462/f63b3a0a-6b91-4776-94d4-47dd86675576">

Output:
<img width="404" alt="Screenshot 2024-02-13 at 9 05 11 PM" src="https://github.com/ArunanSS/cse15l-lab-reports/assets/83483462/6f1108ee-d375-49c7-b89d-f8fe98eb7390">

Sources: "https://www.baeldung.com/linux/recently-changed-files"



How ChatGPT was used to help this: 
Prompt: What are some command line operations that I can use in linux
Output: It gave a variety of operations, but the one I chose to use is find

Prompt: What are some of the command line operations that can be used with examples
Output: I was shown about 20 different examples, I chose the ones I wanted to use then modified them into how they should work



















