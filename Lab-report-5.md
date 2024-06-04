Student: I am having trouble figuring out why my output does not seem like it is correct. I tried different ways of debugging the code but I still can not solve this problem please help. Here is the code and the output.

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
![image](la
