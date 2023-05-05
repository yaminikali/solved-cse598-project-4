Download Link: https://assignmentchef.com/product/solved-cse598-project-4
<br>
The aim of this assignment is to make sure that you have read the slides and the Text Chapter 10 and have understood the concepts covered in the lectures and in the text, including Ado .Net that interfaces SOA software with relational databases, XML databases, and LINQ that deals with different types of databases. By the end of the assignment, you should have a good understanding of the concepts and have applied these concepts in developing operational programs.

<h1>Practice Exercises</h1>

<ol>

 <li>Reading: Textbook Chapter 10.</li>

 <li>Answer the multiple choice questions 1.1 through 1.15 of the text section 10.6. Study the material covered in these questions can help you to prepare for the class exercises, quizzes, and the exam.</li>

 <li>Study for the questions 2 through 8 in text section 10.6. Make sure that you understand these questions and can briefly answer these questions. Studying the material covered in these questions can help you to prepare for the exam and understand the homework assignment.</li>

 <li>Follow the tutorial in text section 10.3.4 to create a LINQ to SQL database, and use LINQ to query the database. Depending on the database that you have installed on your computer and the version of the Visual Studio that you use, the tutorial need to be adjusted based on the features of your software.</li>

 <li>Read and test the following code (Source: https://social.msdn.microsoft.com/). The program processes a .csv (Comma-Separated Values) file, which can be read as a text file. This example can help you in answering your assignment question.</li>

</ol>

<table width="649">

 <tbody>

  <tr>

   <td width="649">int entriesFound = 0; using (var textReader = new StreamReader(“fileName”)) {  string line = textReader.ReadLine();  int skipCount = 0;  while (line != null &amp;&amp; skipCount &lt; 1) {   line = textReader.ReadLine();                      skipCount++;}while (line != null) {   string[] columns = line.Split(_Delimiter);//perform your logic   entriesFound++;   line = textReader.ReadLine();</td>

  </tr>

 </tbody>

</table>




}

}

Explain what this piece of code does.

<h1>Assignment 7       LINQ to Objects Query</h1>

<ol>

 <li>As an example, you are given an Excel file Courses.csv in the “comma separated values” format, which is copied from the ASU course list. The list is modified for the assignment. Do not use the list for scheduling you class. You must add at least 10 classes into the list so that the data are sufficient to show all the features that are required. You will write a program to create an in-memory array from the data source and then query the data source using LINQ to Objects classes. Use comments to indicate what part of code answers which question. You can use a console application or other .Net application template to implement this assignment. You can put the Courses.csv into the App_Data folder in your application.

  <ul>

   <li>Define a Course class consisting of at least the following members: CourseId, Subject, CourseCode, Title, Location, and Instructor. Write a program to read the Courses.csv file and create an in-memory</li>

  </ul></li>

</ol>

<strong>array</strong> of objects of the Course class.                                                                                                   [10]

Hint: Start from the program given in Question 5 in Practice Exercises part.

<ul>

 <li>Create the following LINQ queries to extract data from your in-memory data source.

  <ol>

   <li>Retrieve the list of IEE courses with a course number / code of 300 or higher. Deliver the result set in the type of IEnumerable&lt;T&gt;, where each entity contains course title and course instructor. The result set must be sorted by instructor and in ascending order. Print the results.</li>

  </ol></li>

</ul>

[5]

<ol start="10">

 <li>Retrieve and deliver the courses in groups and subgroups (in two levels): Use the course subject, (e.g., CPI, CSE, and IEE), as the first level key, and use the course code (e.g., 240, 310, and 494) as the second level key. Print the groups that have at least two courses in the second level group. Hint: Read the example in text 10.3.3 and lecture slides 4-2. [10]</li>

</ol>

<ul>

 <li>Create a new file called Instructors.csv. The schema of the file is: instructor name, office number, and email address. Choose at least 30 instructors from Courses.csv list and add them into your Instructors file. You can find the information from CIDSE faculty directory at : https://cidse.engineering.asu.edu/facultyandresearch/directory/faculty/</li>

</ul>

You can make up an office number and the email address if you cannot find the information from the site. Each email address must be unique. You can create the file manually using Excel.     [5]

<ul>

 <li>Define the Instructor class consisting of the following members: InstructorName, OfficeNumber, and EmailAddress. Write a program to read the Instructors.csv file and create an in-memory <strong>list</strong> of the</li>

</ul>

objects of the Instructor class.                                                                                                             [10]

<ul>

 <li>Use the Courses array and Instructors list as two data sources. Write a query to find the course instructor’s email address for each course. Deliver the result set in the type <strong>var</strong>, where each entity contains Subject CourseCode (e.g., CSE 310) and the course’s instructor email address. The result set must be sorted by CourseCode in ascending order. Print the results for all 200 level courses. [10]</li>

</ul>

<h1>Assignment 8        LINQ Application</h1>

<ol start="2">

 <li>For the same Excel file Courses.csv file, in this part of the assignment, you will create an XML document from the data source and query the XML data source using LINQ to XML classes. Use comments to indicate what part of code answers which question. You can use a console application or other .Net application template to implement this assignment. You can put the Courses.csv into the</li>

</ol>

App_Data folder in your application.

<ul>

 <li>Define the Course class consisting of at least the following members: CourseId, Subject, CourseCode, Location, and Instructor. Write a program to read the Courses.csv file and create an in-memory <strong>XML</strong></li>

</ul>

file of the objects of the Course class.                                                                                                 [10]

<ul>

 <li>Save the XML document into the App_Data folder in your application. [10]</li>

 <li>Create the following LINQ queries to extract data from your in-memory XML source.

  <ol>

   <li>Retrieve the list of CPI courses with a course number of 200 or higher. Deliver the result set in the type of IEnumerable&lt;XElement&gt;, where each entity contains course title and course instructor. The result set must be sorted by instructor in ascending order. Print the results. [5]</li>

   <li>Retrieve and deliver the courses in groups in two levels: Use the course subject, (e.g., CPI, CSE, and IEE), as the first level key, and use the course code (e.g., 240, 310, and 494) as the second level key. Print the groups that have at least two courses in the second level group. [10]</li>

  </ol></li>

 <li>Use the Course XML document and Instructors list (created Assignment 7) as data sources. Write a query to find each course and the course instructor’s email address. Deliver the result set in the type IEnumerable&lt;XElement&gt;, where each entity contains Subject and CourseCode (e.g., CSE 310) and course instructor’s email address. The result set must be sorted by CourseCode in ascending order.</li>

</ul>

Print the results for all 200 level courses.