Download Link: https://assignmentchef.com/product/solved-ds-assignment1-sorted-linked-list-and-hash-table
<br>
For this assignment, you will compare the efficiency of searching a sorted linked list and a hash table.  You should use a variation of your code for Mini-Assignment 3 for this.

<strong>Modifications from Mini-Assignment 3</strong>

<ul>

 <li>Instead of getting the words to load into the hash table from the user, you must load at least 2000 words from a file called words.txt as input (using file I/O). It is OK if you share the words with classmates for this. Make sure that your words are sorted in random order (more about this later). The words.txt file must be in the same directory as your source code.

  <ul>

   <li>It’s OK to use more than 2000 words but don’t have more than 10000.</li>

  </ul></li>

 <li>When you load a word into the hash table, also load the words into one very long sorted linked list. You <strong>must </strong>use the same function for inserting into the sorted linked list as for inserting into the hash table bucket’s linked list.</li>

 <li></li>

 <li>Make the hash table 127 buckets in size.</li>

 <li></li>

 <li>You must create a function called searchLinkedList that searches a sorted linked list for a word and returns a pointer to the node containing the word (if found) or NULL.

  <ul>

   <li>This function must return NULL immediately after you pass the point in the linked list where the word would have been found if it was in the linked list.</li>

   <li>The function takes three parameters:

    <ol>

     <li>char * searchWord: word to search for (entered by the user)</li>

     <li>struct linkedList * linkedList: linked list to search (in your program, you can call the linked list node struct anything that makes sense)</li>

     <li>int * comparisonCount: pointer to int filled in by the function with the count of strcmp comparisons done in searching the linked list</li>

    </ol></li>

   <li>Create a search function called searchForWordTwice. It returns nothing and will have the following parameters:

    <ul>

     <li>char * searchWord: word to search for (entered by the user)</li>

     <li>struct linkedList * linkedList: linked list to search</li>

     <li>struct linkedList * hashTable[]: hash table to search</li>

     <li>int comparisonCount[2]: array containing the count of strcmp comparisons done in searching the extremely-long sorted linked list (element 0) and in searching the hash table (element 1)</li>

    </ul></li>

   <li>It must call your linked list search function and then displays one of the following messages once the search is done:

    <ul>

     <li>“<em>word</em>was found in the <em>list</em> in <em>number</em> comparisons”, where <em>word</em> is the word being searched for, <em>list </em>is either “linked list” or “hash table bucket” and <em>number</em>equals the number of times that strcmp was called</li>

     <li>“<em>word</em>was NOT found in the <em>list</em> in <em>number</em> comparisons”</li>

    </ul></li>

   <li>You will use this search function to search the hash table bucket and the sorted linked list.

    <ul>

     <li>Don’t worry about the grammatical inconsistency of possibly displaying “1 comparisons”.</li>

     <li>Indent the message displayed by one TAB (‘t’).</li>

    </ul></li>

   <li>Once you are finished the loop, display the total number of searches, the total number of comparisons done by searching the sorted linked list, and the total number of comparisons done by searching the hash table.</li>

  </ul></li>

</ul>

<strong>Other Requirements</strong>

Design your linked list code so that you do not have to duplicate code unnecessarily. This is very important.

Clean up <strong>all</strong> allocated memory before exiting.

Use constants to avoid magic numbers.

You can assume that all words will be in lowercase.

Your program must compile without warnings. If you have to use a #pragma as stated in the C course notes in order to get rid of the Microsoft-specific warnings, you should do so.  Your project must be named dsA2.  The source file that contains your main() function must be called dsA2.c or dsA2.cpp. Put all hash table-related code in hashing.c or hashing.cpp.  Put all linked list-related code in linkedlist.c or linkedlist.cpp (and linkedlist.h if you are using a class).  Create other .h files as needed to support compilation. Do not create any other source files.  Remember to put appropriate header comments at the top of ALL source files.  Create a JPG file called compare.jpg that contains a screenshot of your program running with a full screen of sample output (so that I can see the difference in comparison count between the methods for multiple <strong>successful and unsuccessful</strong> searches (do not skimp on the number of searches)). Make sure that it <strong>includes the final summary output</strong>. Put this file in the <strong>top directory</strong> of your project (so that it is submitted with your submission). A <a href="https://conestoga.desire2learn.com/content/enforced/203337-PROG1370-102-18S-1_18S_X_B309_PROG1370_SEC1_X/004-Assignments/compare.jpg?_&amp;d2lSessionVal=YsrnUWknwxF3HBR4qZeznNi7E&amp;ou=203337">sample of this file</a> is provided for you. Please follow the output format and contents exactly.

Provide your words.txt file in the same directory as your source code.

Call your ZIP file DSA2.zip.  Submit your submission to the appropriate dropbox as required by the SET Submission Standards document.