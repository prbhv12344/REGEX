# REGEX
RegEx explanation:
A regular expression is a sequence of characters that define a search pattern. It is mainly used for string pattern matching.Regular expressions are extremely useful in extracting information from text such as: code, log files, spreadsheets, documents, etc.
Case sensitive.
Task

You have a test string S . Your task is to match the string hackerrank.(Case sensitive)
JAVA CODE:import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {    

    public static void main(String[] args) {
        
        Regex_Test tester = new Regex_Test();
        tester.checker("hackerrank"); //Pattern matching
    
    }
}

class Regex_Test {

    public void checker(String Regex_Pattern){
    
        Scanner Input = new Scanner(System.in);
        String Test_String = Input.nextLine();
        Pattern p = Pattern.compile(Regex_Pattern);
        Matcher m = p.matcher(Test_String);
        int Count = 0;
        while(m.find()){
            Count += 1;
        }
        System.out.format("Number of matches : %d",Count);
    }   
    
}
