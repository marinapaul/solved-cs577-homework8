Download Link: https://assignmentchef.com/product/solved-cs577-homework8
<br>
<ol>

 <li> Your friends are attending a convention and want to ask questions to the panelists. They worked together to create a set <em>S </em>of <em>n </em>different topics they would like to ask about. Each of your <em>m </em>friends has a VIP pass that guarantees them the ability to ask at most three questions each.</li>

</ol>

Unfortunately, due to the dense subject matter of the convention, not all of your friends understand every topic well enough to ask about it. For each friend <em>i </em>= 1<em>,</em>2<em>,…,m</em>, they have a set <em>S<sub>i </sub></em>of topics they are capable of asking about. Finally, to make sure each topic is thoroughly addressed, the friends want to ask at least <em>k </em>different questions about each of the <em>n </em>topics (Note that one person should not ask about the same topic more than once). They are having trouble figuring out who should ask about which topics.

<ul>

 <li>Design a polynomial-time algorithm that takes the input to an instance of this problem (the <em>n </em>topics, the sets <em>S<sub>i </sub></em>for each of the <em>m </em>friends, and the parameter <em>k</em>) and decides whether there is a way to ask <em>k </em>questions about each of the <em>n </em>topics, while each friend asks at most three questions each.</li>

 <li>You show your friends a solution computed by your algorithm from (a), but to your surprise, one of them exclaims, “That won’t do at all– the first topic is only asked about by Optimists!” You hadn’t heard anything about optimists; this is an extra wrinkle they neglected to mention earlier.</li>

</ul>

Each of your friends is either an Optimist or a Pessimist. This refers to their general attitude- they each fall into exactly one of these two categories and will behave that way for the entire convention, regardless of the topic they are asking about. To keep the panel’s responses as fair as possible, your friends agree that there should be no topic for which all <em>k </em>questions come from people with the same attitude.

Describe how to modify your algorithm from (a) into a new polynomial-time algorithm that decides whether there exists a solution satisfying all of the conditions from (a), plus the new requirements about optimists and pessimists.

<ol start="2">

 <li>The Packers are playing the Bears tonight, and you’d like to invite some of your friends to watch the game at your place. All of your friends love football, and are either Packers or Bears fans, but some of them are known not to get along very well. In order to avoid possible trouble, you do not want to invite two people who are on bad terms with each other <em>and </em>root for a different team. (Having people who are on bad terms but root for the same team is OK, as is any of the other two combinations.) Also, although you like all of your friends, you like some better than others, and you have assigned a positive value to each of your friends.</li>

</ol>

Design a polynomial-time algorithm to figure out which friends to invite so as to maximize their total value under the above constraints.

<h1>Regular problems</h1>

<ol start="3">

 <li>[Graded, 3 points] You’re a homeowner who wants to revitalize your backyard. You make a list of <em>n </em>landscaping projects you want completed. There are two local landscaping companies that can do these jobs for you: Abed’s Azaleas and Britta’s Botanical Boutique. You can designate any subset of the tasks to each company, but every job should be done exactly once. Abed charges <em>a<sub>i </sub></em>to do job <em>i</em>, and Britta charges <em>b<sub>i </sub></em>for the same job. You’d like to spend as little money as possible, but you also need to account for the incompatibilities between the styles of the different suppliers. If you get jobs <em>i </em>and <em>j </em>done by different companies, there is an incompatibility cost of <em>c</em>(<em>i,j</em>).

  <ul>

   <li>Design an efficient algorithm to determine which landscaper should do each task so as to minimize the sum of the purchase costs and incompatibility costs.</li>

   <li>It’s a slow season for the gardening industry, so these two companies are competing hard for your business. You’ll be completing the jobs in the order of your list, and Abed and Britta both have a copy. They’re also fiercely staking out each other’s businesses, so they’ll know when you purchase a service from their competitor. To try to win you back and keep the industry competitive, they both start offering you the same discount: if you recently hired their competitor, they’ll offer you a discount <em>d </em>off your next purchase. More formally, if you purchase job <em>i </em>from one company, the competing company will subtract <em>d </em>from their price to complete job (<em>i </em>+ 1). They aren’t being too generous, though: you can assume <em>d </em>is less than the cost of all jobs, and is also less than all <em>c</em>(<em>i,j</em>).</li>

  </ul></li>

</ol>

Describe what efficient modification you can make to your algorithm from (a) so that your minimum sum of purchase costs and incompatibility costs accounts for this discount.

<ol start="4">

 <li>Some of your friends with jobs out West decide they really need some extra time each day to sit in front of their laptops, and the morning commute from Woodside to Palo Alto seems like the only option. So they decide to carpool to work.</li>

</ol>

Unfortunately, they all hate to drive, so they want to make sure that any carpool arrangement they agree upon is fair, and doesn’t overload any individual with too much driving. Some sort of simple round-robin scheme is out, because none of them goes to work every day, and so the subset of them in the car varies from day to day.

Here’s one way to define fairness. Let the people be labeled <em>S </em>= {<em>p</em><sub>1</sub><em>,…,p<sub>k</sub></em>}. We say that the <em>total driving obligation </em>of <em>p<sub>j </sub></em>over a set of days is the expected number of times that <em>p<sub>j </sub></em>would have driven, had a driver been chosen uniformly at random from among the people going to work each day. More concretely, suppose the carpool plan lasts for <em>d </em>days, and on the <em>i</em>th day a subset <em>S<sub>i </sub></em>⊆ <em>S </em>of the people go to work. Then the above definition of the total driving obligation ∆<em><sub>j </sub></em>for <em>p<sub>j </sub></em>can be written as ∆. Ideally, we’d like to require that <em>p<sub>j </sub></em>drives at most ∆<em><sub>j </sub></em>times; however, ∆<em><sub>j </sub></em>may not be an integer.

So let’s say that a driving schedule is a choice of a driver for each day -— i.e., a sequence <em>p<sub>i</sub></em><sub>1</sub><em>,p<sub>i</sub></em><sub>2</sub><em>,…,p<sub>i</sub></em><em><sub>d </sub></em>with <em>p<sub>i</sub></em><em><sub>t </sub></em>∈ <em>S<sub>t </sub></em>-— and that a fair driving schedule is one in which each <em>p<sub>j </sub></em>is chosen as the driver on at most d∆<em><sub>j</sub></em>e days.

<ul>

 <li>Prove that for any sequence of sets <em>S</em><sub>1</sub>, …, <em>S<sub>d</sub></em>, there exists a fair driving schedule.</li>

 <li>Design an algorithm to compute a fair driving schedule in time polynomial in <em>k </em>and <em>d</em>.</li>

</ul>

<ol start="5">

 <li>A <em>vertex cover </em>of a graph <em>G </em>= (<em>V,E</em>) is a collection of vertices <em>C </em>⊆ <em>V </em>such that every edge <em>e </em>∈ <em>E </em>has at least one vertex in <em>C</em>.</li>

</ol>

Show that for bipartite graphs, the minimum size of a vertex cover equals the maximum size of a matching.

<h1>Challenge problem</h1>

<ol start="6">

 <li>Here is a variant of the game “Six Degrees of Kevin Bacon.”</li>

</ol>

You start with a set <em>X </em>of <em>n </em>actresses and a set <em>Y </em>of <em>n </em>actors, and two players <em>P</em><sub>0 </sub>and <em>P</em><sub>1</sub>. Player <em>P</em><sub>0 </sub>names an actress <em>x</em><sub>1 </sub>∈ <em>X</em>, player <em>P</em><sub>1 </sub>names an actor <em>y</em><sub>1 </sub>who has appeared in a movie with <em>x</em><sub>1</sub>, player <em>P</em><sub>0 </sub>names an actress <em>x</em><sub>2 </sub>who has appeared in a movie with <em>y</em><sub>1</sub>, and so on. Thus, <em>P</em><sub>0 </sub>and <em>P</em><sub>1 </sub>collectively generate a sequence <em>x</em><sub>1</sub><em>,y</em><sub>1</sub><em>,x</em><sub>2</sub><em>,y</em><sub>2</sub><em>,… </em>such that each actor/actress in the sequence has costarred with the actress/actor immediately preceding. A player <em>P<sub>i</sub></em>(<em>i </em>= 0<em>,</em>1) loses when it is <em>P<sub>i</sub></em>’s turn to move, and she cannot name a member of her set who hasn’t been named before.

Suppose you are given a specific pair of such sets <em>X </em>and <em>Y </em>, with complete information on who has appeared in a movie with whom. A <em>strategy </em>for <em>P<sub>i </sub></em>in our setting is an algorithm that takes a current sequence <em>x</em><sub>1</sub><em>,y</em><sub>1</sub><em>,x</em><sub>2</sub><em>,y</em><sub>2</sub><em>,… </em>and generates a legal next move for <em>P<sub>i </sub></em>(assuming it’s <em>P<sub>i</sub></em>’s turn to move). Design a polynomial-time algorithm that, given some instance of the game, decides at the start of the the game which of the two players can force a win.

<h1>Programming problem</h1>

<ol start="7">

 <li>SPOJ problem <a href="https://www.spoj.com/problems/BANKROB">Bank robbery</a> (problem code BANKROB).</li>

</ol>