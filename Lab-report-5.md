Student: I am having trouble figuring out why my output does not seem like it is correct, it should show the test case and which tests fail and pass. I tried different ways of debugging the code but I still can not solve this problem please help. I think there is a bug in the code. Here is the code and the output. 

```
CPATH='.:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar'

rm -rf student-submission
rm -rf grading-area

mkdir grading-area

git clone student-submission
echo 'Finished cloning'


# Draw a picture/take notes on the directory structure that's set up after
# getting to this point

# Then, add here code to compile and run, and do any post-processing of the
# tests

# step 2: Check that the student code contains The ListExamples.java
if [[ -f student-submission/ListExamples.java ]]
then
    echo "ListExamples.java"
else 
    echo "ListExamples.java not found."
    echo "Grade: 0"
    exit
fi
# step 3: put all relevant files into the grading_area directory
    #TestListExamples.java, ListExamples.java, lib directory 

cp TestListExamples.java student-submission/ListExamples.java grading-area
cp -r lib grading-area

# step 4: compile the java files and checked if they compiled successfully
cd grading-area
javac -cp $CPATH *.java


if [[ $? -eq 0 ]] 
then
    echo "The Exit Code for the compile step is $?."
    echo "All Good."
    javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java 
    java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples.java 

else
    echo "The Exit Code for the compile step is $?."
    echo "There was an error compiling"
    echo "Grade: FAILED!"
fi

# step 5: run the tests and report the grade based on the test result.
```
![image](Lab5-error.png)

Tutor: This could be a problem with the argument with the Git clone area because _____. When trying to do commands in bash and there are arguments, you can try using `$1` up to `9` which represents the arguments so `1` represents the first argument and `$9` represents the ninth argument.

Student: I just tried that right now and it seem like it work however I got another bug but this time in a .java file. Here is the code and output.

```
import static org.junit.Assert.*;
import org.junit.*;
import java.util.Arrays;
import java.util.List;

class IsMoon implements StringChecker {
  public boolean checkString(String s) {
    return s.equalsIgnoreCase("moon");
  }
}

public class TestListExamples {
  @Test(timeout = 500)
  public testMergeRightEnd() {
    List<String> left = Arrays.asList("a", "b", "c");
    List<String> right = Arrays.asList("a", "d");
    List<String> merged = ListExamples.merge(left, right);
    List<String> expected = Arrays.asList("a", "a", "b", "c", "d");
    assertEquals(expected, merged);
  }
}
```
![image](Lab5-error2.png)

Tutor: It seems like you are not returning anything in the testMergeRightEnd() method. You can either make it return something or make it a void method. Being a void means that you dont have to return anything essentially.

Student: Thank you very much, it started to work now.
![image](Lab5-correct.png)
