Download Link: https://assignmentchef.com/product/solved-cs1331-homework-10-enterprise
<br>
<h1>Problem Description</h1>

Since your bizarre time traveling incident from a few weeks ago, you’ve successfully launched your own forum site, helped the owner of a local puppy shelter modernize their business, explored the curious properties of Conway’s Game of Life, and have created a dueling simulator for Professor Dumbledore at Hogwarts. Needless to say, things have been looking up for being trapped in 1998! However, much to your dismay your forum site has had very little activity; apparently no one else has experienced similar time traveling incidents.

However, today that is about to change! Instead of waking up in your bed this morning, you wake up in a futuristic cell, and in a much more comfortable bed. You are greeted by a bizarre humanoid creature with yellow-green, scaly skin. It approaches you, and says, “Good morning, human. I apologize for the previous mishap in our time travel device; it has been acting up due to recent events. My name is Silik, and I am the leader of the Suliban Cabal. You are currently hundreds of light-years away from Earth on my ship, and it is the Earth year 2745. Species around the universe are currently engaged in a Temporal Cold War, which has caused the timeline to become seriously disrupted. My men have taken heavy damage in an attempt to fix it, and we need your help to restore the timeline. We currently lack sufficient technical manpower to restore our database on Starfleet and the history of your species. Because of your great technical ability, you have been selected to create the infrastructure that will restore it. You will start with data representations of humans, androids, and Vulcans; we believe events related to these three species particularly disrupted the timeline. Once your work is complete, we will send you back to your own time so you can resume your studies, but only if you are successful. We have much Java documentation to guide your work, and we will provide an IDE that you are comfortable with. Remember, the timeline depends on your success, so we can’t afford any mishaps. Good luck!”

<h1>Solution Description</h1>

For this assignment, you will be dealing with 3 concrete classes, an abstract class, an enumeration, and 2 interfaces.

The following files are provided to you for your reference. You will have to implement methods declared in them, but you will not have to modify any code in the files themselves:

<ul>

 <li>java</li>

 <li>java</li>

 <li>java</li>

</ul>

In these files, the following methods have been provided:

<h2>Alien.java</h2>

<ul>

 <li>This file contains the Alien <em>abstract class</em>.</li>

 <li>It contains a singular method, <strong>String getHomePlanet();</strong></li>

</ul>

<strong>– </strong>This method will need to be implemented in <strong>Vulcan.java</strong>, which extends it.

<h2>Logic.java</h2>

<ul>

 <li>This file contains the Logic <em>interface</em>.</li>

 <li>It contains a singular method, <strong>boolean isPrime(int num);</strong>

  <ul>

   <li>This method will need to be implemented in both <strong>java </strong>and <strong>Android.java</strong>.</li>

   <li>The Vulcan species is well-known for being calculating and logical, rather than emotional and instinctive like say, humans or Andorians, which is why they implement this interface. Similarly, androids are part human, part machine, so internally they use much precise logic to function!</li>

   <li>Since both Vulcans and androids are “calculating” and logical, it would make sense that they would need mathematical capabilities to perform their decisions.</li>

   <li>See the file itself for implementation details.</li>

  </ul></li>

</ul>

<h2>Rank.java</h2>

<ul>

 <li>This file contains the Rank <em>enumeration </em></li>

 <li>It contains a list of Rank enums to be used in the next 4 listed files. See details below for their specific use cases.</li>

</ul>

You will need to make changes to the following files, and you will be submitting them to Gradescope:

<ul>

 <li>java</li>

 <li>java</li>

 <li>java</li>

 <li>java</li>

</ul>

<h2>Officer.java</h2>

<ul>

 <li>This file contains the <strong>Officer </strong><em>interface</em>.</li>

 <li>It contains 2 <em>abstract </em>methods, <strong>String getName(); </strong>and <strong>Rank getRank();</strong>.

  <ul>

   <li>These methods will need to be implemented in <strong>java</strong>, <strong>Android.java</strong>, and <strong>Human.java</strong>. Since the Cabal’s database only deals with members of these entities that are part of Starfleet, we know that all instances of them will be Starfleet officers, which is why this interface is used. <strong>– </strong>See the file itself for implementation details.</li>

  </ul></li>

 <li>Additionally, there is one method in this file that you have to implement: <strong>default String rankString();</strong>

  <ul>

   <li>See the file itself for implementation details.</li>

  </ul></li>

 <li>Lastly, there is an implemented static String method provided to you, <strong>private String capitalizeEachWord(String rank);</strong>, that will be used in the implementation of <strong>default String rankString();</strong>. No need to modify this method.</li>

</ul>

<h2>Human.java</h2>

<ul>

 <li>This file contains the <strong>Human </strong><em>concrete class</em>.</li>

 <li>This class will implement the <strong>Officer </strong> See <strong>Officer.java </strong>for its requirements.

  <ul>

   <li>For any method overridden from this interface make sure to use the <strong>@Override </strong>annotation directly above each method header.</li>

  </ul></li>

 <li>It will have 2 instance variables, <strong>String name </strong>and <strong>Rank rank</strong>

  <ul>

   <li><strong>name </strong>should never be able to be changed once initialized in the constructor. What keyword would allow us to do this?</li>

   <li><strong>rank </strong>is allowed to be modified after initialization</li>

  </ul></li>

 <li>It should also have exactly one constructor, which takes in <strong>String name </strong>and <strong>int rank</strong>. It should assign <strong>String name </strong>

  <ul>

   <li>However, we must get the Rank enum value corresponding to int rank. A rank of 0 corresponds to ENSIGN, rank of 1 to Rank.LIEUTENANT, and so on. Note that we can only obtain a valid rank if 0 &lt;= rank &lt;= 5.</li>

   <li>So, if int rank is negative or greater than 5, initialize Rank rank to null. Otherwise, obtain the corresponding enum rank using values(), and set Rank rank equal to it.</li>

  </ul></li>

 <li>This class will also implement the overridden methods <strong>public String toString() </strong>and <strong>public boolean equals(Object other) </strong>from <strong>lang.Object</strong>

  <ul>

   <li>For any method overridden from <strong>lang.Object </strong>make sure to use the <strong>@Override </strong>annotation directly above each method header.</li>

   <li>See the file for implementation details.</li>

  </ul></li>

</ul>

<h2>Vulcan.java</h2>

<ul>

 <li>This file contains the <strong>Vulcan </strong><em>concrete class</em>.</li>

 <li>This class will implement the <strong>Officer </strong> See <strong>Officer.java </strong>for its requirements.

  <ul>

   <li>For any method overridden from this interface make sure to use the <strong>@Override </strong>annotation directly above each method header.</li>

  </ul></li>

 <li>This class will also implement the <strong>Logic </strong>

  <ul>

   <li>For any method overridden from this interface make sure to use the <strong>@Override </strong>annotation directly above each method header.</li>

   <li>See <strong>java </strong>for implementation details.</li>

  </ul></li>

 <li>This class will also extend the <strong>Alien </strong>abstract class. See <strong>java </strong>for its requirements. <strong>– </strong>Note that the home planet of a Vulcan is Vulcan!

  <ul>

   <li>For any method overridden from this abstract class make sure to use the <strong>@Override </strong>annotation directly above each method header.</li>

  </ul></li>

 <li>It will have 2 instance variables, <strong>String name </strong>and <strong>Rank rank</strong>

  <ul>

   <li><strong>name </strong>should never be able to be changed once initialized in the constructor. What keyword would allow us to do this?</li>

   <li><strong>rank </strong>is allowed to be modified after initialization</li>

  </ul></li>

 <li>It should also have exactly one constructor, which takes in <strong>String name </strong>and <strong>int rank</strong>. It should assign <strong>String name </strong>

  <ul>

   <li>However, we must get the Rank enum value corresponding to int rank. A rank of 0 corresponds to ENSIGN, rank of 1 to Rank.LIEUTENANT, and so on. Note that we can only obtain a valid rank if 0 &lt;= rank &lt;= 5.</li>

   <li>So, if int rank is negative or greater than 5, initialize Rank rank to null. Otherwise, obtain the corresponding enum rank using values(), and set Rank rank equal to it.</li>

  </ul></li>

 <li>You should create an additional overloaded method <strong>boolean isPrime(int num1, int num2); – </strong>This method overloads the method <strong>boolean isPrime(int num); </strong>from the <strong>Logic </strong> <strong>– </strong>See <strong>Vulcan.java </strong>for its implementation details.</li>

 <li>This class will also implement the overridden methods <strong>public String toString() </strong>and <strong>public boolean equals(Object other) </strong>from <strong>lang.Object</strong>

  <ul>

   <li>For any method overridden from <strong>lang.Object </strong>make sure to use the <strong>@Override </strong>annotation directly above each method header.</li>

   <li>See the file for implementation details.</li>

  </ul></li>

</ul>

<h2>Android.java</h2>

<ul>

 <li>This file contains the <strong>Android </strong><em>concrete class</em>.</li>

 <li>This class will extend the <strong>Human </strong>concrete class. However, no methods will be overridden from that class.</li>

 <li>This class will also implement the <strong>Logic </strong>

  <ul>

   <li>For any method overridden from this interface make sure to use the <strong>@Override </strong>annotation directly above each method header.</li>

   <li>See <strong>java </strong>for implementation details.</li>

  </ul></li>

 <li>This class will <strong>not </strong>have any instance variables! Instead, it will pass <strong>String name </strong>and <strong>int rank </strong>to the constructor of its superclass, <strong>Human</strong>

  <ul>

   <li>Implement a constructor that takes in <strong>String name </strong>and <strong>int rank</strong>. This constructor should call the superclass constructor in <strong>Human</strong>, which takes in the same parameters. This can be accomplishes using the <strong>super </strong></li>

   <li>It should have a second, no-arg constructor that uses constructor chaining with the this keyword to call the other constructor with parameters <strong>“Data” </strong>and <strong>2</strong>.</li>

  </ul></li>

 <li>You should create an additional overloaded method <strong>boolean isPrime(int num1, int num2, int num3);</strong>

  <ul>

   <li>This method overloads the method <strong>boolean isPrime(int num); </strong>from the <strong>Logic </strong> <strong>– </strong>See <strong>Android.java </strong>for its implementation details.</li>

  </ul></li>

 <li>This class will also implement the overridden method <strong>public String toString()</strong>.

  <ul>

   <li>For any method overridden from <strong>lang.Object </strong>make sure to use the <strong>@Override </strong>annotation directly above each method header.</li>

   <li>See the file for implementation details.</li>

  </ul></li>

</ul>

<strong>Important: Make sure each constructor that takes in </strong><strong>String name and </strong><strong>int rank takes them in exactly in that order!</strong>

<strong>Testing your code:</strong>

We have provided a driver class that you can use to test your code:

<ul>

 <li>java</li>

</ul>

You should create your own tests in the main method! Here is what the expected output of the main method we have provided is:

Captain Kirk

Captain Picard

Admiral Forrest

Android Lieutenant Commander Data

Android Lieutenant Commander Data

Commander Spock from Vulcan

Commander T’Pol from Vulcan

Captain Picard Unranked Daniels

false true false true

false true false false

<h1>Rubric</h1>

<ul>

 <li>[12] java

  <ul>

   <li>[12] String rankString() implementation</li>

  </ul></li>

 <li>[25] java

  <ul>

   <li>[5] Correct Constructor and Variables</li>

  </ul></li>

</ul>

∗ [1] Correct placing of final keyword

∗ [1] Correct variable access modifiers

∗ [3] Correct Constructor behavior

<ul>

 <li>[5] Implements Officer methods</li>

</ul>

∗ [1] @Override annotation present for both

∗ [4] Correct behavior for both

<ul>

 <li>[5] toString() method</li>

</ul>

∗ [1] @Override annotation present

∗ [4] Correct behavior

<ul>

 <li>[10] equals() method</li>

</ul>

∗ [1] @Override annotation present

∗ [2] Correct behavior

<ul>

 <li>[38] java

  <ul>

   <li>[5] Correct Constructor and Variables</li>

  </ul></li>

</ul>

∗ [1] Correct placing of final keyword

∗ [1] Correct variable access modifiers

∗ [3] Correct Constructor behavior

<ul>

 <li>[5] Implements Officer methods</li>

</ul>

∗ [1] @Override annotation present for both

∗ [4] Correct behavior for both

<ul>

 <li>[3] Correctly implements Alien method</li>

 <li>[6] Implements Logic method</li>

</ul>

∗ [1] @Override annotation present

∗ [1] Correct behavior

<ul>

 <li>[4] Overloads Logic method</li>

</ul>

∗ [4] Correct behavior

<ul>

 <li>[5] toString() method</li>

</ul>

∗ [1] @Override annotation present

∗ [4] Correct behavior

<ul>

 <li>[10] equals() method</li>

</ul>

∗ [1] @Override annotation present

∗ [9] Correct behavior

<ul>

 <li>[25] java

  <ul>

   <li>[10] Constructors</li>

  </ul></li>

</ul>

∗ [5] 2-argument Constructor

∗ [2] Uses super keyword

∗ [3] Correct behavior

∗ [5] no-argument Constructor

∗ [2] Uses this keyword

∗ [3] Correct behavior

<ul>

 <li>[6] Implements Logic method</li>

</ul>

∗ [1] @Override annotation present

∗ [3] Correct behavior

<ul>

 <li>[4] Overloads Logic method</li>

</ul>

∗ [4] Correct behavior

<ul>

 <li>[5] toString() method</li>

</ul>

∗ [1] @Override annotation present ∗ [4] Correct behavior

<strong>Allowed Imports</strong>

<ul>

 <li>There are no allowed imports for this assignment.</li>

</ul>

<h1>Javadocs</h1>

For this assignment, you will be commenting your code with Javadocs. Javadocs are a clean and useful way to document your code’s functionality. For more information on what Javadocs are and why they are awesome, the <a href="http://www.oracle.com/technetwork/java/javase/documentation/index-137868.html">online overview</a> for them is extremely detailed and helpful.

You can generate the javadocs for your code using the command below, which will put all the files into a folder called javadoc:

$ javadoc *.java -d javadoc

The relevant tags that you need to include are @author, @version, @param, and @return. Here is an example of a properly Javadoc’d class:

<table width="632">

 <tbody>

  <tr>

   <td width="632"><strong>import </strong>java.util.Scanner;<em>/**</em>* This class represents a Dog object<em>.</em>* <strong>@author </strong>George P<em>. </em>Burdell* <strong>@version </strong><em>1.0</em><em>*/ </em><strong>public class </strong>Dog {<em>/**</em>* Creates an awesome dog <em>(</em>NOT a dawg<em>!) */</em><strong>public </strong>Dog() { …}<em>/**</em>* This method takes in two ints and returns their sum* <strong>@param a </strong>first number* <strong>@param b </strong>second number <em>* </em><strong>@return </strong>sum of a and b<em>*/</em><strong>public </strong>int add(int a, int b) {…}}</td>

  </tr>

 </tbody>

</table>

A more thorough tutorial for Javadocs can be found <a href="https://cs1331.gitlab.io/cs1331-style-guide.html">here</a>. Take note of a few things:

<ol>

 <li>Javadocs are begun with /** and ended with */.</li>

 <li>Every class you write must be Javadoc’d and the @author and @verion tag included. The comments for a class should start with a brief description of the role of the class in your program.</li>

 <li>Every non-private method you write must be Javadoc’d and the @param tag included for every method parameter. The format for an @param tag is @param &lt;name of parameter as written in method header&gt; &lt;description of parameter&gt;. If the method has a non-void return type, include the @return tag which should have a simple description of what the method returns, semantically.</li>

</ol>


