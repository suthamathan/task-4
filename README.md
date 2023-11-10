# task-4
completed 
Task 4 
 
1 question 

import java.util.List;
import java.util.stream.Collectors;
import java.util.stream.Stream;

public class StringListConversion {
    public static void main(String[] args) {
        Stream<String> names = Stream.of("aBc", "d", "ef");
        List<String> upperCaseNames = names.map(String::toUpperCase)
                                          .collect(Collectors.toList());
        System.out.println(upperCaseNames);
    }
}


OUTPUT
[ABC, D, EF]
______________________________________________________________________________________________________________________________________________________________________________________________________________________

QUESTION 2


import java.util.Arrays;
import java.util.List;
import java.util.stream.Collectors;

public class NonEmptyStringList {
    public static void main(String[] args) {
        List<String> strings = Arrays.asList("abc", "bc", "efg", "abcd", "", "jkl");
        
        List<String> nonEmptyStrings = strings.stream()
                                              .filter(s -> !s.isEmpty())
                                              .collect(Collectors.toList());
        
        System.out.println("Non-empty strings: " + nonEmptyStrings);
    }
}


OUTPUT

Non-empty strings: [abc, bc, efg, abcd, jkl]

______________________________________________________________________________________________________________________________________________________________________________________________________________________
 QUESTION 3

import java.util.Arrays;
import java.util.List;
import java.util.stream.Collectors;

public class SpecialGifts {
    public static void main(String[] args) {
        List<String> studentNames = Arrays.asList("Alice", "Bob", "Anna", "Alex", "David", "Amy", "Andrew", "Adam", "John", "Amanda");
        
        List<String> studentsWithAGift = studentNames.stream()
                                                     .filter(name -> name.startsWith("A"))
                                                     .collect(Collectors.toList());
        
        System.out.println("Students with names starting with 'A': " + studentsWithAGift);
    }
}


Output 


Students with names starting with 'A': [Alice, Anna, Alex, Amy, Andrew, Adam, Amanda]
______________________________________________________________________________________________________________________________________________________________________________________________________________________

Question4


import java.time.LocalDate;
import java.time.Period;
import java.util.Scanner;

public class AgeCalculator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Enter your birthdate (yyyy-mm-dd): ");
        String input = scanner.next();
        
        LocalDate birthdate = LocalDate.parse(input);
        LocalDate currentDate = LocalDate.now();
        
        Period period = Period.between(birthdate, currentDate);
        
        int years = period.getYears();
        int months = period.getMonths();
        int days = period.getDays();
        
        System.out.println("Your age is: " + years + " years, " + months + " months, and " + days + " days.");
        
        scanner.close();
    }
}


Output


Enter your birthdate (yyyy-mm-dd): 2002-07-11
Your age is: 21 years, 3 months, and 29 days.
______________________________________________________________________________________________________________________________________________________________________________________________________________________

