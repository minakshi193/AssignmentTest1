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
Q2).longest chain

const word = '00000111110101001111100001001';

function findLongestChain(word) {
  let longestChain = '';
  let currentChain = '';

  for (let i = 0; i < word.length; i++) {
    const currentChar = word[i];

    if (currentChar === '1') {
      currentChain += currentChar;
    } else {
      if (currentChain.length > longestChain.length) {
        longestChain = currentChain;
      }
      currentChain = '';
    }
  }

  return longestChain;
}

const longestChain = findLongestChain(word);
console.log('Longest chain of letters:', longestChain);
}

//output//
Longest chain of letters: 1111101

**************************************************************************************************************

Q3).
let obj1 = { "greeting": "hello" };
let obj2 = obj1;
obj1["greeting"] = "bye";
console.log(obj1);
console.log(obj2);

//output//
{ greeting: 'bye' }
{ greeting: 'bye' }

*********************************************************************************************************
Q4).
Console.log("7">7)
Console.log("2">"21")
Console.log("KL">"S")
//output//
false
true
false

****************************************************************************************************************************
q5)
function average(a,b){
return a+b/2;
}
console.log(average(2,1));
}

//output//

the average is 1.5
********************************************************************************************************************************
