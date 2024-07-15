## Experience Sharing: First interview as Senior Dev
---

### Experience Sharing: First interview as Senior Dev

Recently, I had the opportunity to interview for a position at a reputed tech company. I wanted to share my experience, especially the programming questions that were posed during the interview. These questions tested my understanding of Java 8 features and my ability to handle common programming challenges.

#### Question 1: Filtering Countries Starting with 'i'
The first question required me to filter a list of country names and extract those that start with the letter 'i'. The array provided was:

```java
String[] countries = {"india", "indonesia", "america", "china"};
```
I needed to use Java 8 features to achieve this. Here’s the solution I provided:

```java
import java.util.Arrays;
import java.util.List;
import java.util.stream.Collectors;

public class CountryFilter {
    public static void main(String[] args) {
        String[] countries = {"india", "indonesia", "america", "china"};
        Arrays.stream(countries)
            .filter(country -> country.startsWith("i"))
            .forEach(System.out::println); 
    }
}
```

In this solution, I used the stream() method to create a stream from the array, then applied the filter() method to keep only those strings that start with 'i'. Finally, I used forEach to print the results to the console.

#### Question 2: Removing Duplicate Numbers from an Integer Array

The second question was about removing duplicate numbers from an integer array. The array given was something like:

```java
int[] numbers = {1, 2, 2, 3, 4, 4, 5};
```

Here's how I tackled this problem:

```java
import java.util.HashSet;
import java.util.Set;

public class RemoveDuplicatesWithoutStreams {
    public static void main(String[] args) {
        int[] numbers = {1, 2, 2, 3, 4, 4, 5};
        
       Set<Integer> uniqueNumbersSet = new HashSet<>();
        
        for (int number : numbers) {
            uniqueNumbersSet.add(number);
        }
       
        int numberOfDuplicates = numbers.length - uniqueNumbersSet.size();
        System.out.println("Number of duplicates: "+ numberOfDuplicates);
        System.out.print("Unique Array: ");
        uniqueNumbersSet.stream().forEach(elem -> System.out.print(elem + " "));
    }
}
```

In this solution, I decided to go with HashSet as it handles unique values well, then moving onto adding all the elements of array to HashSet to separate duplicate values. Then used the difference in array length and set size to find how many duplicate values where there and then value using stream to print the unique values.

#### Reflection
The interview process was both challenging and enlightening. It reinforced my understanding of Java 8 features like streams and the importance of choosing the right data structures. The experience also highlighted the need to think critically and solve problems efficiently under time constraints.

I hope this post helps anyone preparing for similar technical interviews. Good luck, and happy coding!
