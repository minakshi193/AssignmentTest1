# AssignmentTest1
Q1). find dublicate and same array.

import java.util.ArrayList;
import java.util.HashSet;
import java.util.List;
import java.util.Set;

public class Main {
    public static void main(String[] args) {
        String[] fullwordlist = {"1", "2", "3", "4", "5"};
        String[] wordsToRemove = {"1", "2", "3"};

        // Finding duplicate values
        List<String> duplicateValues = new ArrayList<>();
        Set<String> uniqueValues = new HashSet<>();
        for (String word : fullwordlist) {
            if (!uniqueValues.add(word)) {
                if (!duplicateValues.contains(word)) {
                    duplicateValues.add(word);
                }
            }
        }

        // Finding same values
        List<String> sameValues = new ArrayList<>();
        for (String word : fullwordlist) {
            for (String wordToRemove : wordsToRemove) {
                if (word.equals(wordToRemove) && !sameValues.contains(word)) {
                    sameValues.add(word);
                    break;  // Break out of the inner loop once a match is found
                }
            }
        }

        System.out.println("Duplicate values: " + duplicateValues);
        System.out.println("Same values: " + sameValues);
    }
}
//output//
Duplicate values: []
Same values: [1, 2, 3]

*******************************************************************************************************************
