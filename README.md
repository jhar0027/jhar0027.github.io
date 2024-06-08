# jhar0027.github.io

# jhar0027.github.io

# Application Purpose
This application is designed to assist users in maintaining and tracking volume, intensity, and progress metrics during gym exercises to ensure effective progressive overload. Progressive overload is essential for seeing growth and progress in the gym. The theory of progressive overload involves increasing either repetitions, weight, or sets to continually challenge the body, prompting adaptations for gains. To achieve true growth in the gym, it is essential that users can accurately record their workouts. When completing multiple different exercises with varying weights, sets, and repetitions, it becomes increasingly difficult to remember your previous exercise. Your focus in the gym should be on pushing your body and maintaining proper form to avoid dangerous injuries and facilitate effective growth, rather than trying to remember numerical values in your head. As the body changes, its ability to exert power changes, and it can be dangerous to make large increases to a workout. This application allows the user to make these records for themselves to see growth, ensure loads are increasing, and prevent injury. By creating an application that tracks this progress, users will be more intrinsically motivated through the rewarding action of increasing a value in their workouts and the excitement of trying a new exercise that allows them to add.

# Features of Site
The application allows users to add exercises to their personal exercise portfolio. When the button is clicked a dropdown form created in Javascript. This form is responsive to all screen sizes and will display in full on both mobile and desktop. In this form the user must input the name of the exercise in text form. The user then must select from four categories, Upper body, Lower Body, Cardio, and Other. This is up to the discretion of the user and the site does not categorise these. The user then must submit Sets and Repetitions in numerical value. The date must be input and is not automatically recorded as the date of submission. This allows the user to add records from previous exercises or add records after the exercise. Weights and Image upload are optional due to the variety of exercise styles that may demand no weights at all. Once the user presses the add exercise button, the exercise and information will present under the category the user selected amongst all other exercises. This will remain in the users browser and will allow for persistent access to ensure that the data remains between exercises and workout sessions. The exercise data is also responsive to screen size and is completely visible on screen despite the screen size. The only way for the user to make changes is to reset the site using the delete all exercises button at the footer of the page, far away from the other buttons to prevent from accidental deletion or by deleting an individual exercise record using the x in the corner. There is a search button that allows the user to navigate through their exercises by searching for the exercise title they submitted. The colours yellow and black were used for the colour scheme due to its industrial nature relevant to a gym setting. Yellow is additionally an uplifitng colour and will firther motivate the user to strive for improvement and progress


# Changes made to site
A change was made and a delete button was added for each exercise. This is so the user is able to make changes to one exercise without having to use the “Delete All Exercises” button at the bottom of the screen and start all over again. This may be because they incorrectly entered the weight or sets of one repetition but the other submitted exercises are still correct. The user will not need to restart their records from the beginning but instead just delete the single submission using the x button in the corner, a universally understood symbol. 

The date section in the add exercise form was added. This allowed for more effective record keeping for the user and allowed them to view their progress and compare from their earliest record for the exercise and view their improvement. This is not automatically recorded because users may be submitting their exercises before or after the exercise was complete. This is a necessary submission to the form. 

Instead of the user adding their own categories users will instead pick from four exercises. It is difficult to navigate through a page of over fifty custom categories. In theory to achieve any progressive overload, a continuous repetition of an exercise is necessary thus encouraging the user to make focussed decisions about their exercise. The four chosen categories are upper body, lower body which cover the body parts and cardio section for the non weight training based exercises. The other section would be in for mobility training, flexibility and other unique focuses. 

# References

Resources used for incorporating javascript in the html file
https://www.w3schools.com/js/js_whereto.asp
https://www.digitalocean.com/community/tutorials/how-to-add-javascript-to-html
https://www.digitalocean.com/community/tutorials/how-to-add-javascript-to-html
https://www.w3schools.com/html/html_scripts.asp
https://www.w3schools.com/tags/tag_script.asp

Resources used for searchbar
https://stackoverflow.com/questions/37873005/html-form-action-search-one-text-box-2-buttons-2-possible-results
https://www.w3schools.com/tags/att_form_method.asp
https://medium.com/@kathrynlael/html-forms-post-method-and-search-e2d4ff92abbe
https://www.w3schools.com/howto/howto_css_searchbar.asp
https://stackoverflow.com/questions/51648533/form-action-https-www-google-com-search-method-get-has-to-redirect-to-th
https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/search

### Use of Generative AI 
 **Prompt**

this is my html 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lifit</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap" rel="stylesheet">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=PT+Serif:ital,wght@0,400;0,700;1,400;1,700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header> <!--create the header of the page. this will hold the name of site, search bar and add exercise button. these are the main and most important features of the site and therefore are place at the very top of the page for clear visual heirarchy.-->
        <h1>Lifit</h1> <!--name of application in header-->
        <form action="/search" method="GET"> <!--creates a search form using the http get method -->
            <input type="text" name="query" placeholder="Search">  <!-- the type specifies text. this means that the user will input text to create a form value. "Search" is in the search box when there is no text. this is generally accepted UI for search bars and is univerally understood-->
            <button type="submit">Search</button>  <!-- this creates a button that the user can press to submit thier search. the text "search" has been labeled to the created button as another unerviassly acccepted UI feature-->
        </form>
        <button id="addExerciseButton" onclick="toggleDropdown()">+ Add Exercise</button> <!-- this button is for the user to add an exercise. id reference for css. Java script is used to add dynamic response to thebutton when the button is clicked (see additional information under script tag section in html file below)-->
    </header>
    
    <div id="dropdownForm" class="dropdown-content">  <!--div container created. id created for reference css. class associated for styling-->
        <form id="exerciseForm"><!--form for user input. id of user input created for css reference-->
            <label for="title">Exercise Name:</label> <!--this label is created as a title for the input, as if a categoriser indicating to the user what should be input in this area. for indicated what it is associated with-->
            <input type="text" id="title" name="title" required> <!-- refer to the id created title. this section requires a text input and must have text to submit. This is because there must be a title for the exercise.-->
            
            <label for="category">Category:</label> <!-- creates a descriptive label for the input field. id created for this category name of the category to tell the user what is needed tobe submitted.-->
            <select id="category" name="category" required><!-- select for a dropdown menu, unique id category created. provides namepof selected category and its value is selected form the options. must be selceted to submit form/add exercise-->
                <option value="upper_body">Upper Body</option> <!--multiple options inside the select element. each option is a category users can select. value is for which section of the page the inputs are submitted too. Labels for each exercise type-->
                <option value="lower_body">Lower Body</option> <!--see above-->
                <option value="cardio">Cardio</option> <!--see above-->
                <option value="other">Other</option> <!--see above-->
            </select>
        
            <label for="sets">Sets:</label> <!--creates alabel for the form input. matches the id and the label. has the visible text for context for the user to know what information is to be inputted in this section-->
            <input type="number" id="sets" name="sets" min="1" required> <!-- this is where the user submits data. the only type of data accepted is defined as numerical in the type section. name is forlater form data reference and the minimum is 1 as doing zero sets is not doing the exercise at all --> 
            <label for="repetitions">Repetitions:</label><!--creates a label for the form input.connects the label to the id-->
            <input type="number" id="repetitions" name="repetitions" min="1" required> <!--this is where the user submits data. the only type of data accepted is defined as numerical in the type section. name is forlater form data reference and the minimum is 1 as doing zero repetitions is not doing the exercise at all. must be input to submit the form-->
            <label for="date">Date:</label> <!--creates a label for the form input.connects the label to the id-->
            <input type="date" id="date" name="date" required> 
            <label for="weight">Weight:</label><!--creates a label for the form input.connect the label to the id-->
            <input type="text" id="weight" name="weight"> <!--the type of input is text so that metric system can be specified. its nor arequired field as some exercises do not use weight.-->
            
            <label for="image">Upload Image:</label><!--creates a label for the form input-->
            <input type="file" id="image" name="image"> <!--the type of input is a file uploaded. identifier created. not required to input image to submit form-->
            
            <button type="submit">Add Exercise</button> <!--creates a clickable button. submits the form data. Says "add exercise" on the button to specify to user its feature. no + this time to differnciate and not confuse the user int restarting the submission-->
        </form>
    </div>

    <!--creating sections on page for stand alone data--> <section 
    id="upper_body"> <!-- create identifier-->
        <h2>Upper Body</h2> <!--creates the visible lable for this section on the screen-->
        <div class="exercise-list"></div> <!--create container-->
    </section>
        <!--creating sections on page for stand alone data--><section 
    id="lower_body"><!-- create identifier-->
        <h2>Lower Body</h2><!--creates the visible lable for this section on the screen-->
        <div class="exercise-list"></div><!--create container-->
    </section>
    <!--creating sections on page for stand alone data--><section 
    id="cardio"><!-- create identifier-->
        <h2>Cardio</h2><!--creates the visible lable for this section on the screen-->
        <div class="exercise-list"></div><!--create container-->
    </section>
   <!--creating sections on page for stand alone data--> <section 
    id="other"><!-- create identifier-->
        <h2>Other</h2><!--creates the visible lable for this section on the screen-->
        <div class="exercise-list"></div><!--create container-->
    </section>

    <footer> <!--in the footer so itis away from all other buttons so it is less likely to be accidentally pressed by user-->
        <button id="deleteAllButton">Delete All Exercises</button> <!--creates as button with the text. delete all exercises so it is clear to user the action of this button.-->
    </footer>

    <!--the following is the integrated javascript to make the site more dynamic and responsive with dropdown menus and active buttons -->
    <script>
        function toggleDropdown() { //defining the function. below is run when this function is called above in the created html button
            var dropdown = document.getElementById("dropdownForm");//selecting the dropdownFrom from html id created id="dropdownForm" class="dropdown-content" and creates new name to hold the information" dropdown.
            dropdown.style.display = (dropdown.style.display === "block") ? "none" : "block"; //css display and change to style of html. block to take up width of the page. none is when it take up no space "folded" this creates conditions and displays the dropdown based on what is displayed.true or false to return none or block. toggles between each so that they go back and forth. if its not none it has to be block and if its not block it has to be none= if its not already open it must be trying to open it.
        }

        document.getElementById("exerciseForm").addEventListener("submit", function(event) { //selects the exerciseForm element from the ID created in above html.create an event listener that runs when the form is submitted
            event.preventDefault();//prevents the page from reloading when the form data in input and submitted and instead send it to this javascript tobe unpacked and resubmitted rather than having the code run above.
            const title = document.getElementById("title").value; //this picks the exercise name out from the id created in above html. stores the title in the title category.
            const category = document.getElementById("category").value;//this picks the category of exercise out from the id created in above html. stores the category that the user selected in the categrory cateogry
            const sets = document.getElementById("sets").value;// this picks the number of sets outfrom the id created in above html. stores the number value under the sets variable
            const repetitions = document.getElementById("repetitions").value;//this picks the repitiions out from the id created in above html. stores the number value selected under the repetitions variable
            const weight = document.getElementById("weight").value; //this selcts the wieght input from the id created in above html. stores the value for the weights in the wieghts variable.
            const imageInput = document.getElementById("image");//this selects the input of the image from the id created in above html. gets the file inputted for the image.
            const date = document.getElementById("date").value;//selects the date
            const image = imageInput.files.length > 0 ? URL.createObjectURL(imageInput.files[0]) : ''; //>0 checks if there is a file. if it is zero there is no file if it detects someting there is a file. creates a link for the file so it can be used on the site without rerequesting it from the users device. ? for if there is a like. if there isnt a link then there wasnt an image so dont search for input.

            // Create a new exercise element 
            const exerciseElement = document.createElement("div"); //refers to the html above and creates the new html element div to be created. declares the variable to new div.
            exerciseElement.className = "exercise-item";//set the class for the div from above. assigns for the css too
            /* this allows the html in the div to be defined */ exerciseElement.innerHTML = ` 
            
                <h3>${title}</h3> 
                <p>Sets: ${sets}</p>
                <p>Repetitions: ${repetitions}</p>
                <p>Weight: ${weight}</p>
                ${image ? `<img src="${image}" alt="${title}" />` : ''}
            `; //these are multi line strings. there is embedded expresions that are inserted into the string. heading bold font for title using html command.paragraph elements for the other added elements in the exercise. checks if an image is uploaded or just an empty string. if there is an image then img tag if not then none.

           
            document.querySelector(`#${category} .exercise-list`).appendChild(exerciseElement); //this is to make sure that the exercise is submitted to the right category that was selected in the form.

        
            document.getElementById("exerciseForm").reset(); //selects the part of the html. clears all inputs that have been netered nad returnt eh site to the default.
        });

        document.getElementById("deleteAllButton").addEventListener("click", function() { //refers to the html part. returns the html for the delete button.
           
            const exerciseLists = document.querySelectorAll(".exercise-list"); //finds all the html elements in the class exercise list of each individual exercise and makes a node list

           
            exerciseLists.forEach(list => list.innerHTML = ''); //goes over each element on the exercise lists form the created node list and makes it an empty string instead whcih deletes all the child elements.
        });

    </script>
</body>
</html>

i want each exercise submitted to have the option to to delete. so that theuser can delete just one exercise and they do not need to delete all exercises with the button created in footer. so in the corner of each exercise submitted under each category should have an x to delete the exercise when its clicked on.

**Return**
To allow users to delete individual exercises from the list, you can add a delete button (an "X" button) to each exercise entry. This button will call a JavaScript function that removes the specific exercise from the list. I'll guide you through the necessary changes in both the HTML and JavaScript to achieve this.

HTML and JavaScript Changes
Add a Delete Button to Each Exercise Entry

Modify the part of the JavaScript code that creates a new exercise element (exerciseElement) to include a delete button. Here's how you can modify the innerHTML to include a delete button:

javascript
Copy code
exerciseElement.innerHTML = `
    <div class="exercise-header">
        <h3>${title}</h3>
        <button class="delete-exercise" onclick="deleteExercise(this)">X</button>
    </div>
    <p>Sets: ${sets}</p>
    <p>Repetitions: ${repetitions}</p>
    <p>Weight: ${weight}</p>
    ${image ? `<img src="${image}" alt="${title}" />` : ''}
`;
Implement the deleteExercise Function

Define the deleteExercise function in your <script> section to handle the deletion of an exercise when the "X" button is clicked. This function will remove the parent exerciseElement from the DOM.

javascript
Copy code
function deleteExercise(button) {
    button.parentElement.parentElement.remove();
}
This function uses the button parameter to get the clicked button and remove its parent exerciseElement from the DOM.

Style the Delete Button

Add CSS rules to style the delete button appropriately. For instance, you can make it look like a small "X" in the top right corner of the exercise item.

css
Copy code
.exercise-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.delete-exercise {
    background: none;
    border: none;
    color: #ff0000;
    font-size: 1.2em;
    cursor: pointer;
    margin-left: 10px;
}

.delete-exercise:hover {
    color: #b50000;
}
Here's the complete updated HTML and JavaScript with the changes:

Updated HTML
html
Copy code
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lifit</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=PT+Serif:ital,wght@0,400;0,700;1,400;1,700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Lifit</h1>
        <form action="/search" method="GET">
            <input type="text" name="query" placeholder="Search">
            <button type="submit">Search</button>
        </form>
        <button id="addExerciseButton" onclick="toggleDropdown()">+ Add Exercise</button>
    </header>
    
    <div id="dropdownForm" class="dropdown-content">
        <form id="exerciseForm">
            <label for="title">Exercise Name:</label>
            <input type="text" id="title" name="title" required>
            
            <label for="category">Category:</label>
            <select id="category" name="category" required>
                <option value="upper_body">Upper Body</option>
                <option value="lower_body">Lower Body</option>
                <option value="cardio">Cardio</option>
                <option value="other">Other</option>
            </select>
        
            <label for="sets">Sets:</label>
            <input type="number" id="sets" name="sets" min="1" required>
            <label for="repetitions">Repetitions:</label>
            <input type="number" id="repetitions" name="repetitions" min="1" required>
            <label for="date">Date:</label>
            <input type="date" id="date" name="date" required>
            <label for="weight">Weight:</label>
            <input type="text" id="weight" name="weight">
            
            <label for="image">Upload Image:</label>
            <input type="file" id="image" name="image">
            
            <button type="submit">Add Exercise</button>
        </form>
    </div>

    <section id="upper_body">
        <h2>Upper Body</h2>
        <div class="exercise-list"></div>
    </section>
    <section id="lower_body">
        <h2>Lower Body</h2>
        <div class="exercise-list"></div>
    </section>
    <section id="cardio">
        <h2>Cardio</h2>
        <div class="exercise-list"></div>
    </section>
    <section id="other">
        <h2>Other</h2>
        <div class="exercise-list"></div>
    </section>

    <footer>
        <button id="deleteAllButton">Delete All Exercises</button>
    </footer>

    <script>
        function toggleDropdown() {
            var dropdown = document.getElementById("dropdownForm");
            dropdown.style.display = (dropdown.style.display === "block") ? "none" : "block";
        }

        document.getElementById("exerciseForm").addEventListener("submit", function(event) {
            event.preventDefault();
            const title = document.getElementById("title").value;
            const category = document.getElementById("category").value;
            const sets = document.getElementById("sets").value;
            const repetitions = document.getElementById("repetitions").value;
            const weight = document.getElementById("weight").value;
            const imageInput = document.getElementById("image");
            const date = document.getElementById("date").value;
            const image = imageInput.files.length > 0 ? URL.createObjectURL(imageInput.files[0]) : '';

            const exerciseElement = document.createElement("div");
            exerciseElement.className = "exercise-item";
            exerciseElement.innerHTML = `
                <div class="exercise-header">
                    <h3>${title}</h3>
                    <button class="delete-exercise" onclick="deleteExercise(this)">X</button>
                </div>
                <p>Sets: ${sets}</p>
                <p>Repetitions: ${repetitions}</p>
                <p>Weight: ${weight}</p>
                ${image ? `<img src="${image}" alt="${title}" />` : ''}
            `;

            document.querySelector(`#${category} .exercise-list`).appendChild(exerciseElement);
            document.getElementById("exerciseForm").reset();
        });

        function deleteExercise(button) {
            button.parentElement.parentElement.remove();
        }

        document.getElementById("deleteAllButton").addEventListener("click", function() {
            const exerciseLists = document.querySelectorAll(".exercise-list");
            exerciseLists.forEach(list => list.innerHTML = '');
        });
    </script>
</body>
</html>

Summary
Added a delete button to each exercise entry using the delete-exercise class.
Implemented the deleteExercise function to handle individual deletions.
Updated the CSS to style the delete button and added the .exercise-header class to manage the layout of each exercise item.
This approach gives users the ability to delete individual exercises without affecting the rest of their entries.

**Prompt**
this is my html 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lifit</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap" rel="stylesheet">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=PT+Serif:ital,wght@0,400;0,700;1,400;1,700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header> <!--create the header of the page. this will hold the name of site, search bar and add exercise button. these are the main and most important features of the site and therefore are place at the very top of the page for clear visual heirarchy.-->
        <h1>Lifit</h1> <!--name of application in header-->
        <form action="/search" method="GET"> <!--creates a search form using the http get method -->
            <input type="text" name="query" placeholder="Search">  <!-- the type specifies text. this means that the user will input text to create a form value. "Search" is in the search box when there is no text. this is generally accepted UI for search bars and is univerally understood-->
            <button type="submit">Search</button>  <!-- this creates a button that the user can press to submit thier search. the text "search" has been labeled to the created button as another unerviassly acccepted UI feature-->
        </form>
        <button id="addExerciseButton" onclick="toggleDropdown()">+ Add Exercise</button> <!-- this button is for the user to add an exercise. id reference for css. Java script is used to add dynamic response to thebutton when the button is clicked (see additional information under script tag section in html file below)-->
    </header>
    
    <div id="dropdownForm" class="dropdown-content">  <!--div container created. id created for reference css. class associated for styling-->
        <form id="exerciseForm"><!--form for user input. id of user input created for css reference-->
            <label for="title">Exercise Name:</label> <!--this label is created as a title for the input, as if a categoriser indicating to the user what should be input in this area. for indicated what it is associated with-->
            <input type="text" id="title" name="title" required> <!-- refer to the id created title. this section requires a text input and must have text to submit. This is because there must be a title for the exercise.-->
            
            <label for="category">Category:</label> <!-- creates a descriptive label for the input field. id created for this category name of the category to tell the user what is needed tobe submitted.-->
            <select id="category" name="category" required><!-- select for a dropdown menu, unique id category created. provides namepof selected category and its value is selected form the options. must be selceted to submit form/add exercise-->
                <option value="upper_body">Upper Body</option> <!--multiple options inside the select element. each option is a category users can select. value is for which section of the page the inputs are submitted too. Labels for each exercise type-->
                <option value="lower_body">Lower Body</option> <!--see above-->
                <option value="cardio">Cardio</option> <!--see above-->
                <option value="other">Other</option> <!--see above-->
            </select>
        
            <label for="sets">Sets:</label> <!--creates alabel for the form input. matches the id and the label. has the visible text for context for the user to know what information is to be inputted in this section-->
            <input type="number" id="sets" name="sets" min="1" required> <!-- this is where the user submits data. the only type of data accepted is defined as numerical in the type section. name is forlater form data reference and the minimum is 1 as doing zero sets is not doing the exercise at all --> 
            <label for="repetitions">Repetitions:</label><!--creates a label for the form input.connects the label to the id-->
            <input type="number" id="repetitions" name="repetitions" min="1" required> <!--this is where the user submits data. the only type of data accepted is defined as numerical in the type section. name is forlater form data reference and the minimum is 1 as doing zero repetitions is not doing the exercise at all. must be input to submit the form-->
            <label for="date">Date:</label> <!--creates a label for the form input.connects the label to the id-->
            <input type="date" id="date" name="date" required> 
            <label for="weight">Weight:</label><!--creates a label for the form input.connect the label to the id-->
            <input type="text" id="weight" name="weight"> <!--the type of input is text so that metric system can be specified. its nor arequired field as some exercises do not use weight.-->
            
            <label for="image">Upload Image:</label><!--creates a label for the form input-->
            <input type="file" id="image" name="image"> <!--the type of input is a file uploaded. identifier created. not required to input image to submit form-->
            
            <button type="submit">Add Exercise</button> <!--creates a clickable button. submits the form data. Says "add exercise" on the button to specify to user its feature. no + this time to differnciate and not confuse the user int restarting the submission-->
        </form>
    </div>

    <!--creating sections on page for stand alone data--> <section 
    id="upper_body"> <!-- create identifier-->
        <h2>Upper Body</h2> <!--creates the visible lable for this section on the screen-->
        <div class="exercise-list"></div> <!--create container-->
    </section>
        <!--creating sections on page for stand alone data--><section 
    id="lower_body"><!-- create identifier-->
        <h2>Lower Body</h2><!--creates the visible lable for this section on the screen-->
        <div class="exercise-list"></div><!--create container-->
    </section>
    <!--creating sections on page for stand alone data--><section 
    id="cardio"><!-- create identifier-->
        <h2>Cardio</h2><!--creates the visible lable for this section on the screen-->
        <div class="exercise-list"></div><!--create container-->
    </section>
   <!--creating sections on page for stand alone data--> <section 
    id="other"><!-- create identifier-->
        <h2>Other</h2><!--creates the visible lable for this section on the screen-->
        <div class="exercise-list"></div><!--create container-->
    </section>

    <footer> <!--in the footer so itis away from all other buttons so it is less likely to be accidentally pressed by user-->
        <button id="deleteAllButton">Delete All Exercises</button> <!--creates as button with the text. delete all exercises so it is clear to user the action of this button.-->
    </footer>

    <!--the following is the integrated javascript to make the site more dynamic and responsive with dropdown menus and active buttons -->
    <script>
        function toggleDropdown() { //defining the function. below is run when this function is called above in the created html button
            var dropdown = document.getElementById("dropdownForm");//selecting the dropdownFrom from html id created id="dropdownForm" class="dropdown-content" and creates new name to hold the information" dropdown.
            dropdown.style.display = (dropdown.style.display === "block") ? "none" : "block"; //css display and change to style of html. block to take up width of the page. none is when it take up no space "folded" this creates conditions and displays the dropdown based on what is displayed.true or false to return none or block. toggles between each so that they go back and forth. if its not none it has to be block and if its not block it has to be none= if its not already open it must be trying to open it.
        }

        document.getElementById("exerciseForm").addEventListener("submit", function(event) { //selects the exerciseForm element from the ID created in above html.create an event listener that runs when the form is submitted
            event.preventDefault();//prevents the page from reloading when the form data in input and submitted and instead send it to this javascript tobe unpacked and resubmitted rather than having the code run above.
            const title = document.getElementById("title").value; //this picks the exercise name out from the id created in above html. stores the title in the title category.
            const category = document.getElementById("category").value;//this picks the category of exercise out from the id created in above html. stores the category that the user selected in the categrory cateogry
            const sets = document.getElementById("sets").value;// this picks the number of sets outfrom the id created in above html. stores the number value under the sets variable
            const repetitions = document.getElementById("repetitions").value;//this picks the repitiions out from the id created in above html. stores the number value selected under the repetitions variable
            const weight = document.getElementById("weight").value; //this selcts the wieght input from the id created in above html. stores the value for the weights in the wieghts variable.
            const imageInput = document.getElementById("image");//this selects the input of the image from the id created in above html. gets the file inputted for the image.
            const date = document.getElementById("date").value;//selects the date
            const image = imageInput.files.length > 0 ? URL.createObjectURL(imageInput.files[0]) : ''; //>0 checks if there is a file. if it is zero there is no file if it detects someting there is a file. creates a link for the file so it can be used on the site without rerequesting it from the users device. ? for if there is a like. if there isnt a link then there wasnt an image so dont search for input.

            // Creating a new exercise element 
            const exerciseElement = document.createElement("div"); //refers to the html above and creates the new html element div to be created. declares the variable to new div.
            exerciseElement.className = "exercise-item";//set the class for the div from above. assigns for the css too
            /* this allows the html in the div to be defined */ 
            

            exerciseElement.innerHTML = ` 
            <div class="exercise-header">
                    <h3>${title}</h3>
                    <button class="delete-exercise" onclick="deleteExercise(this)">X</button>
                </div>
                <h3>${title}</h3> 
                <p>Sets: ${sets}</p>
                <p>Repetitions: ${repetitions}</p>
                <p>Weight: ${weight}</p>
                ${image ? `<img src="${image}" alt="${title}" />` : ''}
            `; //these are multi line strings. there is embedded expresions that are inserted into the string. heading bold font for title using html command.paragraph elements for the other added elements in the exercise. checks if an image is uploaded or just an empty string. if there is an image then img tag if not then none.

           
            document.querySelector(`#${category} .exercise-list`).appendChild(exerciseElement); //this is to make sure that the exercise is submitted to the right category that was selected in the form.

        
            document.getElementById("exerciseForm").reset(); //selects the part of the html. clears all inputs that have been netered nad returnt eh site to the default.
        });
        function deleteExercise(button) {
            button.parentElement.parentElement.remove();
        }
        document.getElementById("deleteAllButton").addEventListener("click", function() { //refers to the html part. returns the html for the delete button.
           
            const exerciseLists = document.querySelectorAll(".exercise-list"); //finds all the html elements in the class exercise list of each individual exercise and makes a node list

           
            exerciseLists.forEach(list => list.innerHTML = ''); //goes over each element on the exercise lists form the created node list and makes it an empty string instead whcih deletes all the child elements.
        });

    </script>
</body>
</html>

this is my css

body {
    font-family: "Poppins", sans-serif;
    font-weight: 400;
    font-style: normal;
margin: 0;
padding: 0;
}

header {
text-align: center;
padding: 20px;
background-color: #3B4045;
border-bottom: 1px solid #1E2329;
}

h1 {
font-family: "PT Serif", serif;
font-weight: 700;
font-style: italic;
margin: 0;
font-size: 2.5em;
color: #F5A201;
}

form {
margin-top: 10px;
}

input[type="text"], input[type="number"], select, input[type="file"] {
padding: 10px;
margin: 5px 0;
width: calc(100% - 22px);
font-size: 1em;
border: 1px solid #FED054;
border-radius: 4px;
}

button {
padding: 10px 20px;
font-size: 1em;
border: none;
background-color: #FED054;
color: #1E2329;
border-radius: 4px;
cursor: pointer;
}

button:hover {
background-color: #F5A201;
}

#addExerciseButton {
margin-top: 20px;
}

.dropdown-content {
display: none;
background-color: #E2E1DF;
padding: 20px;
margin: 20px;
border: 1px solid #FED054;
border-radius: 4px;
}

section {
padding: 20px;
margin: 20px;
border: 1px solid #1D2227;
border-radius: 4px;
background-color: #393d424f;
}

.exercise-item {
border: 1px solid #1D2227;
padding: 10px;
margin: 10px 0;
border-radius: 4px;
background-color: #F4C851;
}

.exercise-item img {
max-width: 100%;
height: auto;
border-radius: 4px;
}

.exercise-header {
display: flex;
justify-content: space-between;
align-items: center;
}

.delete-exercise {
background: none;
border: none;
color: #ff0000;
font-size: 1.2em;
cursor: pointer;
margin-left: 10px;
}

.delete-exercise:hover {
color: #b50000;
}

footer {
text-align: center;
padding: 20px;
background-color: #3B4045;
border-top: 1px solid #1E2329;
}

#deleteAllButton {
background-color: #ff0000;
}

#deleteAllButton:hover {
background-color: #b50000;
}

i want to Save the data to the user's browser for persistent access between sessions. idont want this to remove any features i already have. i just want each of the submitted exercises that were input by the user to stay there even when they refresh. dont change any of my other code features

**Return**
To save the data to the user's browser for persistent access between sessions, we can use the Web Storage API, specifically localStorage. This allows us to store data locally in the user's browser and retrieve it even after a page refresh or when the user returns later.

Here’s how you can update your existing code to use localStorage to save and load the exercise data:

JavaScript Changes
Update your script to include functions that save the exercise data to localStorage and load it when the page is initialized.

Add a function to save exercises to localStorage:

This function will collect all exercises from the DOM and save them as a JSON string in localStorage.

Add a function to load exercises from localStorage:

This function will retrieve the stored data from localStorage and populate the page with the saved exercises.

Update the form submission handler to include saving data:

After a new exercise is added, update the localStorage.

Load saved exercises when the page is loaded:

Use the DOMContentLoaded event to load exercises when the page is ready.

Here’s the updated JavaScript with the localStorage integration:

html
Copy code
<script>
    document.addEventListener("DOMContentLoaded", loadExercises);

    function toggleDropdown() {
        var dropdown = document.getElementById("dropdownForm");
        dropdown.style.display = (dropdown.style.display === "block") ? "none" : "block";
    }

    document.getElementById("exerciseForm").addEventListener("submit", function(event) {
        event.preventDefault();
        const title = document.getElementById("title").value;
        const category = document.getElementById("category").value;
        const sets = document.getElementById("sets").value;
        const repetitions = document.getElementById("repetitions").value;
        const weight = document.getElementById("weight").value;
        const imageInput = document.getElementById("image");
        const date = document.getElementById("date").value;
        const image = imageInput.files.length > 0 ? URL.createObjectURL(imageInput.files[0]) : '';

        const exerciseElement = document.createElement("div");
        exerciseElement.className = "exercise-item";

        exerciseElement.innerHTML = `
            <div class="exercise-header">
                <h3>${title}</h3>
                <button class="delete-exercise" onclick="deleteExercise(this)">X</button>
            </div>
            <p>Date: ${date}</p>
            <p>Sets: ${sets}</p>
            <p>Repetitions: ${repetitions}</p>
            <p>Weight: ${weight}</p>
            ${image ? `<img src="${image}" alt="${title}" />` : ''}
        `;

        document.querySelector(`#${category} .exercise-list`).appendChild(exerciseElement);
        saveExercises();
        document.getElementById("exerciseForm").reset();
    });

    function deleteExercise(button) {
        button.parentElement.parentElement.remove();
        saveExercises();
    }

    document.getElementById("deleteAllButton").addEventListener("click", function() {
        const exerciseLists = document.querySelectorAll(".exercise-list");
        exerciseLists.forEach(list => list.innerHTML = '');
        localStorage.removeItem('exercises');
    });

    function saveExercises() {
        const exercises = [];
        document.querySelectorAll(".exercise-item").forEach(item => {
            const category = item.closest("section").id;
            const title = item.querySelector("h3").innerText;
            const date = item.querySelector("p:nth-of-type(1)").innerText.replace('Date: ', '');
            const sets = item.querySelector("p:nth-of-type(2)").innerText.replace('Sets: ', '');
            const repetitions = item.querySelector("p:nth-of-type(3)").innerText.replace('Repetitions: ', '');
            const weight = item.querySelector("p:nth-of-type(4)").innerText.replace('Weight: ', '');
            const imageElement = item.querySelector("img");
            const image = imageElement ? imageElement.src : '';

            exercises.push({ title, category, sets, repetitions, weight, date, image });
        });

        localStorage.setItem('exercises', JSON.stringify(exercises));
    }

    function loadExercises() {
        const exercises = JSON.parse(localStorage.getItem('exercises')) || [];
        exercises.forEach(({ title, category, sets, repetitions, weight, date, image }) => {
            const exerciseElement = document.createElement("div");
            exerciseElement.className = "exercise-item";

            exerciseElement.innerHTML = `
                <div class="exercise-header">
                    <h3>${title}</h3>
                    <button class="delete-exercise" onclick="deleteExercise(this)">X</button>
                </div>
                <p>Date: ${date}</p>
                <p>Sets: ${sets}</p>
                <p>Repetitions: ${repetitions}</p>
                <p>Weight: ${weight}</p>
                ${image ? `<img src="${image}" alt="${title}" />` : ''}
            `;

            document.querySelector(`#${category} .exercise-list`).appendChild(exerciseElement);
        });
    }
</script>
Explanation
Saving Exercises: The saveExercises function collects all exercise items from the DOM, creates an array of objects containing exercise data, and stores it in localStorage.

Loading Exercises: The loadExercises function reads the stored exercises from localStorage and reconstructs the exercise elements on the page.

Form Submission: When a form is submitted, a new exercise is added to the list and saved immediately to localStorage.

Deleting Exercises: When an exercise or all exercises are deleted, the changes are saved to localStorage.

Additional Notes
Image Persistence: Storing images in localStorage can be tricky since URLs created via URL.createObjectURL are only valid for the current session. If you need true persistence, consider uploading the image to a server or converting it to a Base64 string (which could lead to storage limitations).

Date Display: Ensure the date format matches what users input. You may need to format the date appropriately.

By integrating these changes, your exercise data will persist between sessions, enhancing the user experience without modifying the existing functionality of your application.

**Prompt**
function saveExercises() {
            const exercises = [];
            document.querySelectorAll(".exercise-item").forEach(item => {
                const category = item.closest("section").id;
                const title = item.querySelector("h3").innerText;
                const date = item.querySelector("p:nth-of-type(1)").innerText.replace('Date: ', '');
                const sets = item.querySelector("p:nth-of-type(2)").innerText.replace('Sets: ', '');
                const repetitions = item.querySelector("p:nth-of-type(3)").innerText.replace('Repetitions: ', '');
                const weight = item.querySelector("p:nth-of-type(4)").innerText.replace('Weight: ', '');
                const imageElement = item.querySelector("img");
                const image = imageElement ? imageElement.src : '';
    
                exercises.push({ title, category, sets, repetitions, weight, date, image });
            });
    
            localStorage.setItem('exercises', JSON.stringify(exercises));
        }
    
        function loadExercises() {
            const exercises = JSON.parse(localStorage.getItem('exercises')) || [];
            exercises.forEach(({ title, category, sets, repetitions, weight, date, image }) => {
                const exerciseElement = document.createElement("div");
                exerciseElement.className = "exercise-item";
    
                exerciseElement.innerHTML = `
                    <div class="exercise-header">
                        <h3>${title}</h3>
                        <button class="delete-exercise" onclick="deleteExercise(this)">X</button>
                    </div>
                    <p>Date: ${date}</p>
                    <p>Sets: ${sets}</p>
                    <p>Repetitions: ${repetitions}</p>
                    <p>Weight: ${weight}</p>
                    ${image ? `<img src="${image}" alt="${title}" />` : ''}
                `;
    
                document.querySelector(`#${category} .exercise-list`).appendChild(exerciseElement);
            });
        }
explain this code

**Return**
Certainly! Let's break down the saveExercises() and loadExercises() functions in the provided code:

saveExercises() Function:
This function is responsible for saving the exercise data to the browser's localStorage.

Initialize an Empty Array:

const exercises = [];: Creates an empty array to store the exercise data.
Iterate Through Exercise Items:

document.querySelectorAll(".exercise-item").forEach(item => {...});: Selects all elements with the class .exercise-item and iterates over them using forEach.
Extract Exercise Data:

Inside the loop, it extracts various properties of each exercise item:
category: Retrieves the category of the exercise from the closest <section> element's ID.
title: Gets the exercise title from the <h3> element.
date, sets, repetitions, weight: Extracts these values from their respective <p> elements.
image: Checks if the exercise has an image (<img> element) and extracts its src attribute.
Push Exercise Data to Array:

It pushes an object containing the extracted exercise data into the exercises array.
Save to Local Storage:

localStorage.setItem('exercises', JSON.stringify(exercises));: Converts the exercises array to a JSON string and saves it to the browser's localStorage with the key 'exercises'.
loadExercises() Function:
This function is responsible for loading the exercise data from localStorage and populating the exercise list on the page.

Retrieve Exercise Data from Local Storage:

const exercises = JSON.parse(localStorage.getItem('exercises')) || [];: Retrieves the exercise data stored in localStorage with the key 'exercises'. If there's no data or it's invalid JSON, it initializes exercises as an empty array.
Iterate Through Stored Exercises:

It iterates through each stored exercise in the exercises array.
Create Exercise Elements:

For each stored exercise, it creates a new HTML element (<div>), representing an exercise item.
Inside this element, it constructs the HTML structure using the stored exercise data to display the exercise title, details, and optionally, an image.
Append Exercise Element to the Correct Category:

It appends the newly created exercise element to the appropriate category's exercise list based on the stored category data.
This process ensures that when the page is loaded, any previously saved exercises are retrieved from localStorage and displayed in the correct category on the page.
