
<h1> Lesson 2 </h1>
**Part I**
1. Study the Yourdon [2] concept of a design walkthrough and the IBM concept [1] of a design inspection. Discuss the similarities and the differences between them. <br><br>
\-	Both concepts are similar in a way that they are a form of group code reading and that they aim to detect errors in the system. They are different in a way that inspection is highly formal and structured, while walkthrough is not necessary formal and somehow casual. Also, inspection has pre-determined designated roles for all participants, while for walkthrough, yes there is something like this, but it is almost always the author who leads the review with some people assigned in different tasks. <br><br>
2. A software engineering group is developing a mission-critical software system that will launch laser-guided missiles to its destinations. This is a new kind of product that was never built by the company. As a quality assurance manager, which code review methodology—walkthrough or inspection—would you recommend? Justify your answer. <br><br>
\-	The code review methodology that I would recommend is inspection. I prefer inspection over walkthrough in this matter because we are dealing with mission-critical software system, especially one that was never built by the company. Situations like this need proper documentation, consistent defect tracking, and careful consideration which are offered best by inspection over walkthrough. <br><br>
3. What size of a review team would you recommend for the project in exercise 2, and why? What are the different roles of each member of the review team? What groups should send representatives to participate in code review? <br><br>
\-	I recommend that the size of the review team for the project in exercise 2 be about 10-20 people. Usually, review teams consist of only about 5-10 members, but considering that this project is mission-critical, all details must be examined thoroughly and I think that having extra people in the team should help in this matter. In the team there must be: a moderator (who leads the inspection, schedules meetings, controls the meetings, reports inspection results, and follows up on rework issues), an author (who created or maintains the work product being inspected), a reader (describes the sections of the work product to the team as they proceed through the inspection), a recorder (who classifies and documents defects and issues raised during the inspection), and a handful of inspectors or reviewers (who attempt to find errors in the product). All participants act as inspectors, in addition to any other responsibilities. <br><br>
4. Suppose that the C programming language is chosen in the project in exercise 2. Recommend a detailed code review checklist to the review team. <br><br>
\-	**General** <br>
1. 	Does the code do what has been specified in the design specification? <br>
2. 	Does the procedure used in the module solve the problem correctly? <br>
3. 	Does the programmer make consistent use of indentation? <br>
4. 	Does the programmer make consistent use of braces? <br>
5.	Are block comments, one-line comments and inline comments used appropriately? <br>
6.	Is a blank line placed before and after a block comment or a one-line comment to separate it from the surrounding source code? <br><br>
**Variable Declaration, Initialization, Qualifiers, and Scope** <br>
7. 	Are global variables used sparingly? <br>
8. 	Are variable names with leading and/or trailing underscores not used? <br>
9. 	Are the names of constants defined by #define, enumerated constants, and constants defined with a specific data type all in CAPITAL letters? <br>
10. 	Are variables names which differ only by case not used? <br>
11.	Do variable names not conflict with standard library function names? <br>
12.	Variable names are descriptive.<br>
13.	Is a consistent format for the naming of variables used? <br>
(Words in the names of local variables are distinguished either by separating them by underscores or by using camel case with the leading letter of the variable in lower case) <br>
14.	Are pointers initialized to NULL? <br>
15.	Are pointers tested for NULL before being referenced? <br>
16.	Is the “const” qualifier used for variables whose value should not be modified? <br>
17.	Is the “static” qualifier applied to all file scope variables and functions whose use is local to a single file? <br>
18.	Are static variables initialized when they are declared? <br>
19.	Are local arrays which are initialized using an initializer list made static?  <br>
	(They are should be made const if their contents are not to be modified) <br>
20.	Are constants declared in header files? <br>
21.	Are values not hard coded? <br>
22.	Are loop index variable names short? <br>
23.	Are pointer variables named in a consistent fashion? <br><br>
**Pointers and Dynamic Memory** <br>
24.	Is dynamically allocated memory deallocated when no longer needed? <br>
25.	Do functions not return pointers to non-static stack dynamic variables? <br>
26.	Are large arrays dynamically allocated on the heap? <br><br>
**Functions** <br>
27.	Is a consistent format for the naming of functions used? <br>
(Words in function names are distinguished either by separating them by underscores or by using camel case with the leading letter of the function name in lower case) <br>
28.	Are function prototypes declared in header files which are included in the source modules that call the functions? <br>
29.	Are the arguments specified in function prototypes associated with variable names? <br>
	(The variable names match the variable names in the function definitions) <br>
30.	Are functions used only in the source module they are created in preceded by the “static” keyword? <br>
	(They do not have prototypes in header files) <br>
31.      Are the return types of functions explicitly stated? <br>
32.	Are standard C Library routines used where appropriate? <br>
33.	Are functions“inlined” if they are small and called many times? <br> 
34.	Is the number of library function calls limited in large loops? <br>
35.	Are embedded statements avoided, minimizing the possibility of side effects? <br>
36.	Are pointers used as arguments to functions in place of passing by value large user-defined types or structures? <br><br>
**User Defined Types** <br>
37.	Are enumerations used to group logically-related constants? <br>
38.	Are macros used judiciously? <br>
39.	Are parentheses used in macros to ensure correct evaluation order? <br>
40.	Are structures used to reduce the number of function calling arguments? <br><br>
**Program Control** <br>
41.	Is unnecessary code avoided in loops? <br>
42.	Is the number of loop counters kept to a minimum. <br>
43.	Are loopscombined when possible to reduce the total loop overhead costs? <br>
44.	Are logical tests optimized by performing the fastest and most capable test first? <br>
45.	Are non-boolean variables tested against an explicit value? <br>
46. 	Is the “goto” statement used sparingly? <br><br>
**C Program Performance** <br>
47.	Are multiple char variables used to store Boolean values rather than using the bits in a byte to represent Boolean flags. <br>
48.	Is the memset C library routine used to initialize large areas of memory? <br>
49.	Is the memcpy C library routine used to copy large areas of memory? <br>
50.	Are frequently read files or database tables read once and buffered in memory? <br>
51.	Is the form x++ or x-- used rather than x=x+1 or x+=1 or x-=1 when possible? <br>
52.	Is multiplication of integer variables by powers of 2 done with left shifts? <br>
53. 	Is division of integer variables by powers of 2 done with right shifts? <br>
54.	Is sorting and searching large amounts of data done using appropriate and efficient techniques? <br>
55.	Are repetitive computations reduced by doing them once and saving the results in temporary variables for future access? <br><br>
5. In addition to code review, what other static unit testing techniques would you recommend for the project in exercise 3? Justify your answer. <br><br>
\-	In my perspective, I would not recommend other static unit testing techniques because inspection is the best one for the said mission-critical system.  <br><br>
6. Describe the special role of a record keeper. <br><br>
\-	As the name of the role implies, a record keeper simply documents the problems found and follow-up actions suggested. Along with this, he or she transcribes the description of the problem, priority, person assigned for follow-up, and the target date for fixing. <br><br>
7. Discuss the importance of code review rework and validation. <br><br>
\-	In a code review, rework and validation are very essential parts. Reviews would be pointless if there will not be any improvements in the system. This is where rework comes in. In this part, the author works on documented problems to be fixed and realizing improvement opportunities, considering the agreed-upon timeframe or deadline. At the same time, the author documents the improvements he or she made to the code. After rework is where validation comes in. This is where the moderator or a person designated for this purpose ensures that the suggested improvements are implemented correctly. We do not aim to just mindlessly ‘implement’ improvements in the code via rework, but we also ensure quality by validation. <br><br>
**Part II** (Note: Refer to your previous software developed) <br>
1. Attempt to draw a control flow graph for a module that you have recently developed. Determine the cyclomatic complexity for the module. Is the module too complex? <br><br>

```
    bool validPrice(char priceInput[12]) {
(1)	  int dotcount = 0;
(2)	  bool ret = true;
	
(3)	  for ((3a) int i = 0; (3b) i < strlen(priceInput); (3c) i++) {
(4)		    if (isdigit(priceInput[i]))
  		     continue;
(5)  		  else if (priceInput[i] == '.')
(6)  		  dotcount++;
(7)  		  else {
(8)  		  	  printf("   Invalid input for price!\n");
(9)  		   	 ret = false;
			         break;
  		     }

(10)  		 if (dotcount > 1) {
(11)  		   	printf("   Invalid input for price!\n");
(12)  		   	ret = false;
			         break;
  		     }   
      }
(13)  return ret;
     }
```
<br><br>

![Control Flow Graph](http://i.imgur.com/MrFQ0xQ.png) <br><br>
**Cyclomatic Complexity = Number of edges – number of nodes = 18 – 15 = 3** <br>
I believe it is not ‘too complex’, but it is unnecessarily ‘complex’ because of redundant statements or lines of code. <br><br>

2. For your previous software project, conduct a formal code review as described in Section 3.2. Since this is by pair, choose only one software project for the code review. <br><br>

- [x]    1. Does the code do what has been specified in the design specification?
- [x]    2. Does the procedure used in the module solve the problem correctly?
- [ ]	 3. Does a software module duplicate another existing module which could be reused?
- [x]	 4. If library modules are being used, are the right libraries and the right versions of the libraries being used?
- [x]  	 5. Does each module have a single entry point and a single exit point? Multiple exit and entry point programs are harder to 		    test.
- [ ]  	 6. Is the cyclomatic complexity of the module more than 10? If yes, then it is extremely difficult to adequately test the 		    module.
- [x]  	 7. Can each atomic function be reviewed and understood in 10–15 minutes? If not, it is considered to be too complex.
- [ ]    8. Have naming conventions been followed for all identifiers, such as pointers, indices, variables, arrays, and constants? It is important to adhere to coding standards to ease the introduction of a new contributor (programmer) to the development of a system.
- [ ]    9. Has the code been adequately commented upon?
- [x]	 10. Have all the variables and constants been correctly initialized? Have correct types and scopes been checked?
- [x]	 11. Are the global or shared variables, if there are any, carefully controlled?
- [x]	 12. Are there data values hard coded in the program? Rather, these should be declared as variables.
- [x]	 13. Are the pointers being used correctly?
- [ ]    14. Are the dynamically acquired memory blocks deallocated after use?
- [ ]    15. Does the module terminate abnormally? Will the module eventually terminate?
- [ ]    16. Is there a possibility of an infinite loop, a loop that never executes, or a loop with a premature exit?
- [x]    17. Have all the files been opened for use and closed at termination?
- [ ]    18. Are there computations using variables with inconsistent data types? Is overflow or underflow a possibility?
- [x]    19. Are error codes and condition messages produced by accessing a common table of messages? Each error code should have a meaning, and all of the meanings should be available at one place in a table rather than scattered all over the program code.
- [ ]    20. Is the code portable? The source code is likely to execute on multiple processor architectures and on different operating 	     systems over its lifetime. It must be implemented in a manner that does not preclude this kind of a variety of execution           	     environments.
- [ ]    21. Is the code efficient? In general, clarity, readability, or correctness should not be sacrificed for efficiency. Code 		     review is intended to detect implementation choices that have adverse effects on system performance. 

