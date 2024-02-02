# NP HTML5, CSS3, and JavaScript 6e Tutorial 14, Case Problem 2


## instruction:

```

1.  Use your editor to open the cc_staff_txt.html and cc_staff_txt.js files from the html14 > case2 folder. Enter your name and the date in the comment section of each file, and save them as cc_staff.html and cc_staff.js respectively.

2.  Go to the cc_staff.html file in your editor. Within the document head, add script elements for the cc_data.js and cc_staff.js files in that order. Load the files asynchronously. Take some time to study the contents of the file and then close it, saving your changes.

3.  Use your editor to open the cc_data.js file and study the data stored in the staff object to become familiar with its contents and structure. Close the file, but do not make any changes to the document.

4.  Go to the cc_staff.js file in your editor. Richard has already created a constructor function for the class of employee objects storing each employee's id, name, department, position, e-mail, phone, and photo. He has also already created an object literal named searchResult that will be used to store the search results in an employees array.

5.  Go to the event listener for the click event. This event listener will run the code that displays the search results in a staff table. Within this event listener, add the code specified in Steps 6 through 19.

6.  Richard has added the removeChildren() method to the prototype of the HTMLElement object that removes all children from a DOM element. Apply this method to the tableBody variable to remove all table rows that might still be present in the staff table from previous searches.

7.  Erase previous search results by setting the employees array of the searchResult object to the empty array [].

8.  Next, you will write the code that returns the employee records that match search conditions set by the user. Apply the forEach() array method to loop through the contents of the direc¬tory array in the staff object. For each employee object in the directory array, run an anonymous function with the parameter, record, that represents each record in the array. Add the commands specified in Steps 9 through 15 to the anonymous function within the forEach() array method.

9.  Create the namesearch variable equal to the value entered in the nameSearch input box.

10.  Users can search for names in three ways: 1) Matching an employee's last name if it contains the text string specified in nameSearch, 2) Matching an employee's last name if it begins with the nameSearch text string, and 3) Matching an employee's last name only if it exactly matches the nameSearch text string. Richard has supplied you with code to add the selectedValue() method to the prototype of the HTMLSelectElement object class in order to return the value of the selected option in any selection list. Apply the selectedValue() method to the nameSearchType selection list to return the option selected by the user, storing the value in the namesearchType variable.

11.  Create a switch-case structure for the following possible values of the nameSearchType variable:
    a.  If nameSearchType equals "contains", use the new RegExp() constructor to create a regular expression object named nameRegExp containing the regular expression nameSearch where nameSearch is the value of the nameSearch variable. Include the "i" flag with the regular expression object so that the regular expression matches lowercase or uppercase characters.
    b.  If nameSearchType equals "beginsWith", set nameRegExp object to the regular expression ^nameSearch, once again with the "i" flag.
    c.  If nameSearchType equals "exact", set nameRegExp object to the regular expression AnameSearch$ with the "i" flag to allow for uppercase and lowercase matches.

12.  Using nameRegExp as the regular expression, apply the test() method to the record.Lastname property (the last name stored in the employee record currently being examined in the forEach() loop). Store the results of the test() method in the foundName variable.

13.  Repeat Steps 9 through 12 to determine whether the employee's position property matches the value entered into the positionSearch input box on the web form. Store the value of the positionSearch input box in the positionsearch variable, the type of search in the positionsearchType variable, the regular expression in the positionRegExp variable, and the result of the regular expression test in the foundPosition variable.

14.  The final search condition in the web form allows the user to specify the employee's department. Users can leave the department blank (to match any department) or they can specify the department from the deptSearch selection list. Apply the selectedValue() method that Richard created for select elements to the deptSearch selection list to retrieve the department value selected by the user, storing the value in the deptsearch variable. If deptSearch equals "" or the value of record.dept (the value of the dept property for the current employee record currently being examined in the forEach() loop), store the Boolean value true in the deptFound variable.

15.  For an employee record to be displayed in the staff table, it must match the search condition set by the user. Insert an if statement that tests whether foundName, foundPosition, and foundDept are all true. If so, use the push() method to add a new employee object to the employees array in the searchResult object. (Hint: use record.id, record.firstName, record.lastName, and so on as the parameter values in the new employee() statement.)

16.  After the forEach loop has finished and the employees array in the searchResult object contains all of the employee records matching the user's search conditions, change the text content of the tableCaption object to "total records found" where total is the value of the length of the employ¬ees array in the searchResult object.

17.  Apply the sortById() method to the searchResult object, which will sort the content of the employees array by the employee ID number.

18.  Finally, add a table row to the body of the staff table: one row for each employee record. Apply the forEach() method to employees array in the searchResult object and for each record in the array, append the following document fragment to the tableBody object <tr> <td><img src="photo" /></td> <td>first last</td> <td>dept</td> <td>position</td> <td><a href="mailto:email">email</a></td> <td><a href="tel:phone">phone</a></td> </tr> where photo, first, last, dept, position, email, and phone are the values of the photo, firstName, lastName, dept, position, email, and phone property of the current record in the employees array of the searchResult object.

19.  Document your work on the application with descriptive comments and then save your work.

20.  Open the cc_staff.html file in your browser. Verify that you can use the Search form to search for employees based on their last name, department, and position. Further verify that you can apply the Contains, Begin With, and Exact options for matching the employee's last name and position in the company.


```