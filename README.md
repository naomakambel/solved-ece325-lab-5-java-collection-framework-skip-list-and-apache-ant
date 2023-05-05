Download Link: https://assignmentchef.com/product/solved-ece325-lab-5-java-collection-framework-skip-list-and-apache-ant
<br>
A <em>collection</em> (sometimes called a container) is simply an object that groups multiple elements into a single unit. Collections are used to store, retrieve, manipulate, and communicate aggregate data. Typically, they represent data items that form a natural group, such as a poker hand (a collection of cards), a mail folder (a collection of letters), or a telephone directory (a mapping of names to phone numbers).

A <em>collection framework</em> is a unified architecture for representing and manipulating collections. All collection frameworks contain the following:

<ul>

 <li><strong>Interfaces</strong>: These are abstract data types that represent collections. Interfaces allow collections to be manipulated independently of the details of their representation. In object-oriented languages, interfaces generally form a hierarchy.</li>

 <li><strong>Implementations</strong>: These are the concrete implementations of the collection interfaces. In essence, they are reusable data structures.</li>

 <li><strong>Algorithms</strong>: These are the methods that perform useful computations, such as searching and sorting, on objects that implement collection interfaces. The algorithms are said to be <em>polymorphic</em>: that is, the same method can be used on many different implementations of the appropriate collection interface. In essence, algorithms are reusable functionality.</li>

</ul>

——————————————————————————–

| ——————————————————-  ——————- |

| |                    ————–                   |  |     ——-     | |

| |                    | Collection |                   |  |     | Map |     | |

| |                    ————–                   |  |     ——-     | |

| |        +———–+—–+——+————+      |  |  ————-  | |

| |     ——-    ———    ———    ———  |  |  | SortedMap |  | |

| |     | Set |    | List  |    | Queue |    | Deque |  |  |  ————-  | |

| |     ——-    ———    ———    ———  |  |                 | |

| |        |                                            |  |                 | |

| |  ————-                                      |  |                 | |

| |  | SortedSet |                                      |  |                 | |

| |  ————-                                      |  |                 | |

| ——————————————————-  ——————- |

——————————————————————————–

The <em>core collection interfaces</em> encapsulate different types of collections, which are shown in the figure below. These interfaces allow collections to be manipulated independently of the details of their representation. Core collection interfaces are the foundation of the <em>Java Collections Framework</em>. Note that all the core collection interfaces are <strong>generic</strong>.

<h1>2  Skip Lists</h1>

Skip lists are designed to overcome the basic limitations of array-based and linked lists — either search or update operations require linear time. It is also an example of a probabilistic data structure, because it makes some of its decisions at random.

<table width="22">

 <tbody>

  <tr>

   <td width="22">Set</td>

  </tr>

 </tbody>

</table>

<table width="48">

 <tbody>

  <tr>

   <td width="48">HashMap</td>

  </tr>

 </tbody>

</table>

As <em>balanced trees</em> (an example is the red black tree) have been used to efficiently implement  and  style data structures, skip list can be an alternative solution. Traditional balanced tree algorithms require continually rebalancing the tree, while skip list provides improved constant time overhead. Besides, search, insert and deletion are rather simple to understand and implement.

In a traditional linked list, each node contains one pointer to the next node. However, a node in a skip list contains an array of pointers. The size of this array, also called the <em>level</em> of the node, is chosen at random at the time when the node is created. For example, a level 3 node has 3 forward pointers, indexed from 0 to

<ol start="2">

 <li>The pointer at index 0 (called the level 0 forward pointer) always points to the immediate next node in the list, and the other pointers point to further nodes. A level<sub>i</sub> pointer points to the next node in the list that satisfy level &gt;= i. Level of the skip list equals to the max level of all its nodes.</li>

</ol>

—                            —-                                    —

2 | |===========================&gt;|  |===================================&gt;||

|-|            —-            |–|            —-            —-    ||

1 | |===========&gt;|  |===========&gt;|  |===========&gt;|  |===========&gt;|  |===&gt;||

|-|    —-    |–|    —-    |–|    —-    |–|    —-    |–|    ||

0 | |===&gt;|  |===&gt;|  |===&gt;|  |===&gt;|  |===&gt;|  |===&gt;|  |===&gt;|  |===&gt;|  |===&gt;||     —    —-    —-    —-    —-    —-    —-    —-    —-    —    head     5       25      30      31      42      58      62      69     null

<h1>3  Apache ANT</h1>

A defined build process is one of the most necessary tools in the software development process, ensuring that the software you produce is built to the required specifications. You should establish, document, and automate the exact series of steps required to correctly build your product.

A defined build process helps close the gap between the development, integration, test and production environments. A build process alone will speed the migration of software from one environment to another. It also removes many issues related to compilation, library paths, or properties that cost many projects considerable time and money.

From this, ANT (originally an acronym for “Another Neat Tool”), a Java-based build tool with special support for Java programming language, has emerged. It helps programmers to build complex applications and place the files in the desired location with less effort. ANT executes different tasks using Java classes and XML-based configuration files.

An ANT build file comes in the form of an XML document. All you need is a simple text editor to edit an

ANT build file. The ANT installation comes with a JAXP-compliant XML parser, which means the

<table width="35">

 <tbody>

  <tr>

   <td width="35">javac</td>

  </tr>

 </tbody>

</table>

installation of an external XML parser is not necessary. The parser checks that the syntax of your ANT file is correct in a similar fashion to  which checks the syntax of your Java code.

<h1>4  Deliverable 1 — Skip List</h1>

Please refer to <em>SkipList.java</em>. For this lab assignment, you need to explore the Java Collections Framework to write a skip list class.

<table width="126">

 <tbody>

  <tr>

   <td width="61">ArrayList</td>

   <td width="23"> or</td>

   <td width="42">Vector</td>

  </tr>

 </tbody>

</table>

<em>Note</em>: it is acceptable if you use the  to store elements. However, remember a skip list

<table width="126">

 <tbody>

  <tr>

   <td width="61">ArrayList</td>

   <td width="23"> or</td>

   <td width="42">Vector</td>

  </tr>

 </tbody>

</table>

is a linked list — this means <strong>the only element that can be directed accessed is the head</strong>, and you have to travel through elements to find the one you need. Elements in  can be accessed by

<strong>DEMO this deliverable to the lab instructor (20 points).</strong>

<h1>5  Deliverable 2 — ANT Build File</h1>

In this step, you need to compile and run your code using ANT.

<em>Step 1: </em>

<table width="22">

 <tbody>

  <tr>

   <td width="22">src</td>

  </tr>

 </tbody>

</table>

Copy and paste your source code (all java files) into  folder in your home directory.

<em>Step 2: </em>

<table width="22">

 <tbody>

  <tr>

   <td width="22">src</td>

  </tr>

 </tbody>

</table>

Consider the sample ANT build file <em>build.xml</em>. Put it in the same directory with your  folder.

If you focus on each of the target tags, you can see how the targets are strung together by a series of dependant attributes. We can see that jar depends on compile, and run depends on jar. What does this

<table width="669">

 <tbody>

  <tr>

   <td rowspan="2" width="353">

    <table width="121">

     <tbody>

      <tr>

       <td width="22">jar</td>

       <td width="77">, and finally</td>

       <td width="22">run</td>

      </tr>

     </tbody>

    </table>mean? Well, if we tell ANT to make the project by target first, and then .<em>Step 3: </em></td>

   <td width="22">


    <table width="20">

     <tbody>

      <tr>

       <td width="20">run</td>

      </tr>

     </tbody>

    </table></td>

   <td rowspan="2" width="214">, then it will automatically perform</td>

   <td width="48">


    <table width="46">

     <tbody>

      <tr>

       <td width="46">compile</td>

      </tr>

     </tbody>

    </table></td>

   <td rowspan="2" width="33"> </td>

  </tr>

  <tr>

   <td width="22"> </td>

   <td width="48"> </td>

  </tr>

 </tbody>

</table>

Now I know about ANT, what do I need to do to allow the following commands to complete successfully?

$ ant -projecthelp

$ ant compile

$ ant jar

$ ant run

ANT can dramatically reduce the overhead related to compiling, archiving and executing your projects.

<em>Step 4: </em>

<table width="691">

 <tbody>

  <tr>

   <td width="358">Change the default target for this build file. Change the</td>

   <td width="114">default=”compile”</td>

   <td width="22"> to</td>

   <td width="88">default=”run”</td>

   <td width="109">, and then run:</td>

  </tr>

  <tr>

   <td colspan="5" width="691">$ ant run</td>

  </tr>

 </tbody>

</table>

Now by default, when you execute ANT, it will automatically compile, build a jar file and execute the code.