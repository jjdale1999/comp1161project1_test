# A test suite for comp1161 project1


First thing is first let us create a jar file for your project.

Your project structure should look something like this. **Before you begin MAKE SURE all your .java files have the line ```package contact;``` at the top**

```
project
|_____bin
│
|_____docs
|
|______src
    │
    |_______contact
            | Adress.java
            | Contact.java
            | Person.java
            | Gender.java
            | Name.java
            | Phone.java
```

## Compiling files
Open a command prompt/terminal to the project folder.N.B (If you want to open a command prompt to the folder just open a command prompt then type ```cd <path_to_the_project_folder>```)

Now type the following. 
#### On Windows
``` 
javac -cp .\src\ .\src\contact\*.java -d .\bin\ 
```

#### On Unix(Mac/Linux)
``` 
javac -cp ./src/ ./src/contact/*.java -d ./bin/ 
```
This compiles your java classes and sets the classpath and stores the output in the bin folder.

## Create Manifest File
Create a folder called **resources** inside your project folder and inside that create a file called **MANIFEST.FM**  (**In your code editor you can create a new file but be sure to select no extension**)

In that file place the following
```
Manifest-Version: 1.0
Class-Path: .

```
Your folder structure should now look like this.

```
project
|____resources
     | MANIFEST.FM
|
|_______bin
│
|_____docs
|
|______src
    │
    |_______contact
            | Address.java
            | Contact.java
            | Person.java
            | Gender.java
            | Name.java
            | Phone.java
```

## Create JAR File
***Note if you use eclipse or any other ide such as intellij you can export the project as a jar file. Just make sure to name it project.jar and you can skip this step.***

#### On Windows

``` 
jar cvfm project.jar .\resources\MANIFEST.FM -C .\bin\ . 
```

#### On Unix(Linux/Mac)
``` 
jar cvfm project.jar ./resources/MANIFEST.FM -C ./bin/ . 
```

A jar file called *project.jar* should have been created in the project folder


## Running the tests

Download the zip https://github.com/stonecoder19/comp1161project1_test/archive/master.zip of this project and extract it. After which open a terminal/command prompt in the extracted folder.

Copy the **project.jar** file to this folder.

The folder structure should like this
```
comp1161project_test
|____
     | AddressTest.java
     | ContactTest.java
     | PersonTest.java
     | NameTesT.java
     | PhoneTest.java
     | junit-4.7.jar
     | hamcrest-all-1.3.jar
     | project.jar
```

#### On Windows

```
javac -cp project.jar;junit-4.7.jar;hamcrest-all-1.3.jar;. .\*.java 
```
```
java -cp project.jar;junit-4.7.jar;hamcrest-all-1.3.jar;. org.junit.runner.JUnitCore AddressTest ContactTest NameTest PhoneTest PersonTest
```

#### Unix(Mac/Linux)
```
javac -cp project.jar:junit-4.7.jar:hamcrest-all-1.3.jar:. ./*.java 
```
```
java -cp project.jar:junit-4.7.jar:hamcrest-all-1.3.jar:. org.junit.runner.JUnitCore AddressTest ContactTest NameTest PhoneTest PersonTest
```

## Results

If you passed all the tests then you should see something similar below, if not then your solution is incorrect. Correct it and repeat all the steps.
``` 
JUnit version 4.7
......................
Time: 0.071

OK (22 tests)
```

## Possible Errors
- If you have an error regarding Gender, make sure the make a seperate file called Gender.java and in that file put the enum e.g 
```java 
    public enum Gender{
        MALE, FEMALE
    }
```
- Make sure the getAddress and the getPhoneList returns a String[]
- Make sure the toString of the Phone is formatted properly eg. (876) 555-5555

## Javadoc Instructions
### Windows
``` 
javadoc -d .\docs .\src\contact\*.java
```
### Unix (Mac\Linux)
```
javadoc -d ./docs ./src/contact/*.java
```

## Submission Instructions

- Now it is time to submit, make sure you copy your jar file to your project folder. Rename your project folder your id number.Folder structure should look something like this for a person with id number 6200000.

```
6200000
|
|_______bin
|
|_______src
|
|_______docs
| 
| project.jar
```
- After you have done this zip this folder and name this zip file your id number e.g. 6200000.zip
- Upload





