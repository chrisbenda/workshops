---
layout: post
title:  "Get started with Network Analyis"
date:   2014-11-09 18:49:00
categories: tech
---

##Goals

Neo4j is a NOSQL database that allows for coding relationships between things. Cypher is the query language that allows us to create the nodes and relationships between things and then ask questions of them. In this class we will create a small graph of the Borges story "On Exactitude in Science" noting the complexity of the story and illustrating some of the patterns that allowed for this complexity.

##Graphing for textual analysis
This is a short video that introduces the concepts we will use while graphing the Borges short story.
![video](http://www.library.vanderbilt.edu/webimages/graphs/video.png)
https://youtu.be/Zgkmbk-Qf_4

This is an image of the graph noted in the video that was created to illustrate some possible connections in the Flannery O'connor short story "The Life You Save May Be Your Own".
![The Life You Save May Be Your Own](http://www.library.vanderbilt.edu/webimages/graphs/life.png)

## What you will need to do in order to complete the class

1) Log in to your Github account or set one up. You can very easily do this at https://github.com/. If you don't know what Github is, it will all be explained at the Github website.

2) In a separate window, navigate to http://gist.neo4j.org/.

3) Read the short story "On Exactitude in Science"By Jorge Louis Borges. It is very short but also very complex so it is a good text to use when learning about graphing for textual analysis. (http://www.sccs.swarthmore.edu/users/08/bblonder/phys120/docs/borges.pdf)

## Creating the data model
Data modeling can be very simple and hand drawn. Below is an illustration of a hand drawn data model that was later coded into a Neo4j graph.

![Data Model](http://www.library.vanderbilt.edu/webimages/graphs/graph.png)

##Cypher-the Neo4j Query language
Now we will look at a very simple graph that has been coded with Cypher to express generic nodes and relationships. Your job will be to modify the cypher to change the variables to something meaningful. In order to do this, go to: copy the gist and create a new gist in your own github account. Once you have done this and you have the URL, go to the open window at  http://gist.neo4j.org/

![Graph Gist](http://www.library.vanderbilt.edu/webimages/graphs/practicegraph.png)

and paste the url of the gist into the search box in the upper right hand corner of the page. If you scroll down the page you will see a graph that looks like this:

Once you are on this page, click  the Page Source button at the top left of the page and you will now be able to edit the code, once you select the edit button in the upper right corner of the page, scroll down until you see this Cipher code.
<div>
=== OUR DATASET
[source, cypher]
----
CREATE
//People
(a:Person{name:'a'}),
(b:Person{name:'b'}),
(c:Person{name:'c'}),

//Places
(d:Location{name:'d'}),
(e:Location{name:'e'}),

//Relationships
(a)-[:R]->(b),
(b)-[:S]->(c),
(b)-[:T]->(d),
(c)-[:U]->(a),
(e)-[:Z]->(b)
</div>

----
to make changes to the code put a real person's name into the first "People" node like this:
<div>
(a:Person{name:'Donald Trump'}),
</div>
You can do the same thing for any of the other People or Places nodes. Now create a relationship between two nodes that you have configured. It might look something like this:
<div>
(a)-[:KNOWS]->(b),
</div>
or

<div>
(a)-[:IS_FROM]->(b),
</div>
After creating a few more examples, you are ready to move on to creating a data model for the short story.

###On Exactitude in Science
Though the story is only one paragraph long, Borges has woven into the narrative many levels of interpretation. No one graph of the story can ever include all of the threads, allusions, associations and levels (unless of course as in the story itself, the map becomes the territory) but it is illuminating to try and encode some of these in a graph.

First, create a data model. It might look something like this:

Or it might be completely different. It really depends on YOUR understanding of the story and how you want to express that understanding as a graph.

Next, using the Cypher example from the first activity above, create nodes and relationships as outlined by your data model. Here is an example of what a very simple graph might look like. Yours can be as simple or as complex as you want it to be.



##Value of Graphing for literary analysis

As noted in the video at the start, good readers have always been close readers. Modelling a short story in this way can help us see beyond the surface narrative and perhaps help us glimpse the glimmering warp and weft of the inner story. It is really just another way to annotate a text, something students and scholars have always done.   


##Next Steps