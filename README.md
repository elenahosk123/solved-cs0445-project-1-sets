Download Link: https://assignmentchef.com/product/solved-cs0445-project-1-sets
<br>



In this assignment, you are given two ADT interfaces, and you will implement them according to their specifications.

Starting point

Download and extract these materials. Contained are:

<ul>

 <li>Driver.java, the provided driver program.</li>

 <li>Movie.java, the things that will be held by a MovieShelf</li>

 <li>SetFullException.java, an exception type</li>

 <li>SetInterface.java and MovieShelfInterface.java, interfaces which you will implement in…</li>

 <li>Set.java and MovieShelf.java. <strong>These are the files you will modify.</strong></li>

</ul>




<h2>Set</h2>

You will implement the Set class. It implements SetInterface. <strong>Read the doc comments for each method in </strong><strong>SetInterface</strong><strong> carefully.</strong> In addition to the interface methods, you will also need to make some constructors, as detailed below.

<strong>Never write an entire program before testing it.</strong> No one writes a correct program in one shot. Save often. Test early and test often. Read the sections of the textbook starting at <strong>Chapter 2.16.</strong>

<h3>Details of your Set implementation</h3>

<ul>

 <li>It will store its data in an array.</li>

 <li>It will be dynamic capacity (like we talked about in Lecture 3).</li>

 <li>The Set(int) constructor will initialize the array to the given capacity.

  <ul>

   <li>It will check for an illegal capacity, and throw IllegalArgumentException in that case.</li>

  </ul></li>

 <li>The Set() constructor will initialize the array to a <em>reasonable default capacity.</em>

  <ul>

   <li>Reusing methods/constructors is a great habit! See section <strong>D.10</strong> of Carrano (page 877 in the 4th edition) for details.</li>

  </ul></li>

 <li>The Set(E[]) constructor will initialize the set to contain the items in the array.

  <ul>

   <li>You <strong>will not</strong> make this array into the set’s backing array. That violates encapsulation.</li>

   <li>The array may contain duplicates and nulls. You should ignore these instead of throwing an exception.</li>

   <li><strong>Do not duplicate your effort.</strong> This is essentially just adding all the items in the array to the set.</li>

  </ul></li>

 <li>Although you are given SetFullException, your add method will <em>never</em> actually throw it.

  <ul>

   <li>Since your implementation will dynamically resize its capacity, it can never be “full.”</li>

  </ul></li>

</ul>

<h2>MovieShelf</h2>

You will implement the MovieShelf class. It implements MovieShelfInterface. Again, read the doc comments in that file carefully.

You are writing code that <strong>uses your own code.</strong> We call this “eating our own dogfood”. It’s kind of a gross term, but hey.

MovieShelf is a <em>client</em> of your Set. That is, it will have an instance of Set and use it to hold its data. This means you are creating this class via <em>composition.</em>

<h3>Details of your MovieShelf implementation</h3>

<ul>

 <li>It will store its data in a Set&lt;Movie&gt;.</li>

 <li>The MovieShelf() constructor will initialize that Set to be empty.</li>

 <li>The MovieShelf(Movie[]) constructor will initialize that Set with that array of Movies.</li>

 <li>A note on printAll(): you can use Set.toArray() to get the movies to print, but it is an array of Object. You will have to cast each item to a Movie to access its movie-specific getters.</li>

</ul>

<h2>Testing</h2>

<strong>We will be testing your code on the command line.</strong> You are welcome to use an IDE, but before submitting, please test that your Java files can be compiled and run on the command line without it.

You are given a simple driver program, <strong>but you should write your own driver as well</strong> to test your code more thoroughly. The driver provided does not test all the possible corner cases, and does not test Set directly.

Click here for an example of what the driver will output for a correct implementation.

<strong>DO NOT TURN IN CODE THAT DOES NOT COMPILE.</strong>

This is not acceptable in this class or in your following classes. Comment out the code that doesn’t compile and put comments at the top of your Java files for the grader. You may receive some partial credit for such code.

Code that crashes may also receive partial credit.