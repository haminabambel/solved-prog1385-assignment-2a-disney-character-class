Download Link: https://assignmentchef.com/product/solved-prog1385-assignment-2a-disney-character-class
<br>
Believe it or not, you have all had the lessons necessary to begin writing your own classes!  One of the scariest things is to do it for the first time … this exercise will ease you through it.  In order to minimize the scary factor – you will be developing a class to model Disney Characters (Mickey, Minnie, etc.) – because hey – there’s nothing scary about Mickey Mouse! (Right? J)

In this exercise, you will be

<ul>

 <li>Using source-code repositories again (as you did in SEF last semester) to store your code for this assignment</li>

 <li>Developing 3 source files to store in your repository o h – the file that contains the class definition for this exercise</li>

</ul>

o    DisneyCharacter.cpp – the source file that contains the method bodies (the code) for the class o       testDisneyCharacter.cpp – your <em>testharness</em> (main function) which you will use to test your class

The requirements description below give you details on the DisneyCharacter class in terms of the data-members (attributes) of the class as well as the methods.

<h1>STEP 1 – Connecting to your Source Repository and Checking in the Initial Solution</h1>

<ol>

 <li>Follow the instructions in the <u>Creating-A-RiouxSVN-Repository</u> document as well as the <u>Installing-Tortoise-SVN</u> document in order to create and prepare your computer for connecting to your personal repository code space.</li>

 <li>As instructed in the <u>Installing-Tortoise-SVN</u> document in eConestoga, create a local directory on your computer (or even one of the lab computers) and call it <strong>C:SETRepo</strong></li>

 <li>Connect to your repository (remembering your repository’s URL and your login credentials using the Tortoise SVN client and perform an <em>SVN Checkout</em>)</li>

 <li>Now start Visual Studio (VS) and create an <strong><u>empty</u></strong> project called DisneyCharacter in the <strong>C:SETRepo</strong> directory (as show in Diagram 1 at the end of this document)</li>

 <li>Let’s setup the skeleton of the source files for this project …

  <ul>

   <li>Add a file called DisneyCharacter.h to the <em>Header Files</em> section in the VS Solution.</li>

   <li>Add a file called DisneyCharacter.cpp to the <em>Source Files</em> section in the VS Solution and</li>

   <li>Also add a file called testDisneyCharacter.cpp to the Source Files</li>

   <li>This is shown in Diagram 2 at the end of this document – just so that the files weren’t empty, I placed a single line comment at the start of each file.</li>

  </ul></li>

</ol>

You do the same.

<ol start="6">

 <li>The reason I wanted to ensure that the source files weren’t empty is because I want to <strong>add</strong> and <strong>commit</strong> the files to my repository now</li>

 <li>When adding VS solutions to a repository – you <strong><em>do not want to add all files </em></strong>that are generated by VS.  This is because some of the files change each and every time you open the solution, or are different on different people’s computers …

  <ol>

   <li>Imagine you were working on a project with a number of other people – all from the same source files. If all VS files were committed – then each and every member of the team would have commits to do every time they opened the project – even if they made no source code changes!!</li>

  </ol></li>

 <li>So now – save the VS solution and project and exit VS. Go to the C:SETRepoDisneyCharacter folder and erase the DEBUG folder.  Then go into the C:SETRepoDisneyCharacterDisneyCharacter folder and erase that DEBUG folder. You do not need or want these 2 folders in your golden copy of the repository,

  <ol>

   <li>As well, if you venture into the C:SETRepoDisneyCharacter.vs folder (which is hidden) and drill further down into the “…DisneyCharacterv15” folder, you may very well see a folder titled <strong>ipch</strong>. Erase this folder – this is where VS hides the incremental pre-compiled header files … these files take up unnecessary space in your repository.</li>

   <li>Once you’ve erased these files and folders – go back to the C:SETRepo folder and right-click on the top-level <strong><u>DisneyCharacter</u></strong> folder (as shown in</li>

  </ol></li>

</ol>

Diagram 3)

<ol>

 <li>Choose the <em>Tortoise-SVN</em> option from the pop-up and the <em>Add</em>  option from the sub-menu – follow the prompts</li>

 <li>Right-click on the same folder again and select <em>SVN Commit</em> – remember when prompted for a commit comment – we want to follow best practices – so give it a comment … perhaps “initial commit of DisneyCharacter solution and project directory structure and files”</li>

</ol>

<ol start="9">

 <li>Now your VS Solution and Project are ready to go, you have skeleton source files and they have been added to your repository …

  <ol>

   <li>You are ready to proceed to Step 2 below – the class definition requirements and coding …</li>

   <li>Please refer to Step 3 below for instructions on saving (updating) your code in your repository (if you complete this exercise over multiple programming sessions). This section also discusses the <em>due-date</em> for this exercise.</li>

  </ol></li>

</ol>




<u>STEP 2 – The Requirements and Programming</u>

This should be a simple one … I want you to write a class definition for a class to be known as <strong>DisneyCharacter</strong>.  Here are the particulars of the class:




<h1>      The Class Particulars</h1>

<ul>

 <li>The class has the following data members name

  <ul>

   <li>a <em>string<a href="#_ftn1" name="_ftnref1"><sup><strong>[1]</strong></sup></a></em> of maximum 50 characters</li>

   <li>if upon construction of the DisneyCharacter object or modification of the name data-member, the name is being set to a <em>string</em> longer than 50 character – you need to truncate the string at 46 characters and append the character sequence “ …” to the end (that is a leading space before the “…” creationDate</li>

   <li>a <em>string</em> of the format yyyy-mm-dd (example value  “2012-01-30”) numMovies</li>

   <li>an integer representing the number of movies that the character has been in whichPark</li>

   <li>a single character value indicating which of the DisneyWorld / DisneyLand parks the character can be found in – allowable values are:</li>

  </ul></li>

 <li>‘M’ for Magic Kingdom</li>

 <li>‘S’ for Disney Studios</li>

 <li>‘A’ for Animal Kingdom</li>

 <li>‘E’ for Epcot</li>

 <li>‘C’ for California Adventure</li>

 <li>‘N’ to indicate the character is not placed</li>

</ul>




<ul>

 <li>The class should have the following methods o a constructor which takes values for all 4 attributes and sets them</li>

 <li>need to ensure that the name <em>string </em>length is not exceeded – otherwise do as required</li>

 <li>need to ensure that incoming value for whichPark data member is valid. If not, mark the character as <em>Not Placed</em>.</li>

 <li>need to ensure that incoming value for numMovies is greater than or equal to zero. If not, set to zero.</li>

 <li>need to ensure that incoming value for creationDate is in the required format. If not, leave blank o        a constructor which takes only the <strong>name</strong> and <strong>creationDate</strong> attributes and defaults the <strong>numMovies</strong> attribute to a value of 0, and the <strong>whichPark</strong> attribute to ‘N’</li>

 <li>need to ensure that the name <em>string </em>length is not exceeded – otherwise do as required</li>

 <li>need to ensure that incoming value for creationDate is in the required format. If not, leave blank</li>

 <li>no other input validation is necessary in this constructor o a destructor</li>

 <li>which prints out message to say “&lt;name attribute&gt; destroyed.” When invoked</li>

 <li>e.g if the DisneyCharacter is “Tigger” then it states “Tigger destroyed”</li>

 <li>accessors for <em>each</em> of the attributes</li>

 <li>a mutator for each of the <strong>numMovies</strong> and <strong>whichPark</strong> attributes

  <ul>

   <li>your mutator’s – like good mutators should perform validation on the incoming parameter value</li>

   <li>and only set the data-member’s value if the incoming value is valid</li>

   <li>if the value is not valid – then the current value for the data-member is left alone</li>

   <li>your mutator should also return a <strong><em>bool</em></strong> data-type to indicate whether the incoming value was valid or not o also declare the following public methods</li>

   <li>ShowInfo(void) – this method is called in order to print out the current value of all of the data members for the object</li>

   <li>In presenting the information to the user … <strong><em>think like the user</em></strong> … what makes sense – what would be understandable to them?</li>

   <li>PlaceCharacter(char whichPark) – this method is called in order to place or position the character at a particular park</li>

   <li>SameMovies(DisneyCharacter&amp; anotherCharacter) – this method is called upon to set the number of movies that this Disney Character has been in to the same number of movies as the specified character (from the parameter list)</li>

  </ul></li>

</ul>




<ul>

 <li>Please follow and use <em>best practices</em> in terms of <strong>encapsulation</strong> o If you are not sure what I mean by this requirement – ask me …</li>

 <li>Place only the class definition in the .H file and <strong><u>place all of the method body code in the .CPP file</u></strong></li>

 <li>Commenting the source code is <strong><em>not required in this exercise</em></strong></li>

</ul>




<u>The Test-Harness Particulars</u> • Your <em>testharness</em>  source code module (i.e. your main() function) is called upon to use the DisneyCharacter class interactively.  In this code: o Instantiate a DisneyCharacter object called mickey  (i.e. name=“Mickey”, creationDate=”1929-01-01”, numMovies=100, whichPark=’M’) o Instantiate  a DisneyCharacter object called minnie  (i.e. name=“Minnie”, creationDate=”1930-01-01”) o try setting the number of Minnie’s movies equal to Mickey’s by calling the SameMovies() method

<ul>

 <li><u>Question</u>: Which object (Minnie or Mickey) is this method called on – and which object (Minnie or Mickey) is passed into it as a parameter? o try dumping out the object’s member values by calling ShowInfo() – for both Mickey and Minnie</li>

</ul>

o    try placing Minnie in the Epcot park.




<h1>STEP 3 – Putting your Code back into the Repository</h1>

Once you’re done programming the exercise – or just want to take a break … you need to save it to your repository.  So save all open files in VS and exit it.

<ul>

 <li>Using Windows Explorer – go back to <strong>C:SETRepo </strong></li>

 <li>You should notice that the Tortoise SVN icons on the folders and files have changed o Please note that depending on the College network – this may or may not work.  There is a background process that runs on the computers called “TSVNCache” which is always connecting to your repository and seeing if your local copy of the files has changed or is different than what is in the repository

  <ul>

   <li>You may see something like Diagram 4 (at the end of this document)</li>

  </ul></li>

 <li>When committing your source code changes to any repository, <em>best practices</em> say that you <strong><u>need to commit each individual source code file</u></strong> (i.e. each .H and</li>

</ul>

.CPP (or whatever language you are programming in)) <strong><u>by itself</u></strong> o          We do this so that our commit message to the repository (which becomes part of the file’s change log) is specific to the changes that you made in that file and that file alone!

<ul>

 <li>So go into your C:SETRepoDisneyCharacterDisneyCharacter directory and <strong>right-click<em> SVN-Commit</em></strong>

  <ul>

   <li>On DisneyCharacter.h – enter a commit comment specific to the changes you made in that file</li>

   <li>On DisneyCharacter.cpp – enter a commit comment specific to those changes and finally</li>

   <li>On testDisneyCharacter.cpp – and enter a commit comment specific to that file</li>

  </ul></li>

 <li>You would do this individual file level commit for all files (usually source file) that you care to have individual commit messages on. In larger system solutions, this may also include configuration files, text files, etc.</li>

</ul>

<ul>

 <li>Just as a catch-all commit after you’ve commited each source file – go back to the <strong>C:SETRepo</strong> directory o If TSVNCache is operating correctly and keeping the SVN icons up-to-date on your directory and files – you may still see a red exclamation mark on the DisneyCharacter folder

  <ul>

   <li>It might be a good idea – until you get the hang of a repository to go back to the top-level directory of your solution (after you’ve committed the individual files that you know you’ve changed separately) and do a <strong>right-click <em>SVN Commit</em></strong> here

    <ul>

     <li>So – you should be in <strong>C:SETRepo</strong> and you right-click and commit on the top-level DisneyCharacter folder</li>

    </ul></li>

   <li>If there really are no more modified files (i.e. files which are different in your local copy than in the repository) – then the commit “files” window will be blank – and you’re done !</li>

   <li>If there are some files that are different in your local copy – they should be VS administration-type files only – and these are safe</li>

  </ul></li>

</ul>

to commit en-masse with one commit comment




<a href="#_ftnref1" name="_ftn1">[1]</a> You can choose to use a char[] for this data member or a string object … either way, you still need to be able to limit the maximum length to 50 characters …