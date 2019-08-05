---
layout:	post
title:	"Sequence Diagrams and better operations planning."
date:	2015-04-05
tags: military agile
---

  I’ve helped plan brigade and battalion level operations in my time as a staff officer and company commander. Lots of staff officers and NCOs standing over a map, drawing symbols on acetate, scribbling notes on paper and into emails and documents. Once the drawing is done one or several staff officers walks away from the table and copies all of the graphics onto power point slides and the Command Post of the Future (CPoF). They also produce the all important narrative for the OPORD/FRAGO/WARNO.

### What I’ve never been as much of a fan of is the fact that map overlays are not great at showing the sequence of events.

Acetate is great, I love that everyone is standing there and planning visually. I think it is a great tool. I’m not a huge fan of the time it takes to make and distribute the copies but I think for planning and discussing it is great and certainly better than trying to plan on separate computers or PowerPoint or even CPoF (which still tracks me as better for operations tracking then operational planning).

The narrative in the OPORD is also an indispensable tool, but it can be hard to read and really grasp the entire flow of events after reading it. They are also really hard to keep consistent. If you make a change in the Scheme of maneuver, did you also update the timeline in coordinating instructions? Or the concept of fires? Annex H? Tasks to subordinate?

Also nothing is worse than spending hours writing and polishing a product, then handing it to a company commander who only skips ahead to their specified tasks, ignoring everything else.

What I've never been as much of a fan of is the fact that map overlays and narratives are not great at showing the sequence of events. The narrative might have all of the exacting detail required to execute, but it is a wall of words, and hard to digest. You end up spending a lot of time flipping between the narative and the map, or multiple map overlays trying to see the flow.

What I propose is to borrow the [Sequence diagram](http://www.agilemodeling.com/artifacts/sequenceDiagram.htm) from the [Unified Modeling Language (UML)](http://www.uml.org/). UML is a modeling and diagraming standard originally designed for software programing and application design.


> Modeling is an Essential Part of large software projects, and helpful to medium and even small projects as well. A model plays the analogous role in software development that blueprints and other plans (site maps, elevations, physical models) play in the building of a skyscraper. Using a model, those responsible for a software development project’s success can assure themselves that business functionality is complete and correct, end-user needs are met, and program design supports requirements for scalability, robustness, security, extendibility, and other characteristics,*before* implementation in code renders changes difficult and expensive to make. ([UML.org](http://www.omg.org/gettingstarted/what_is_uml.htm))Replace “software project” with “military operations” in the above quote and you can easily nest that set of tools into the following from [FM 5–0](http://armypubs.army.mil/doctrine/DR_pubs/dr_a/pdf/adp5_0.pdf):


> The Army design methodology is a methodology for applying critical and creative thinking to understand, visualize, and describe unfamiliar problems and approaches to solving them. Army design methodology is an iterative process of understanding and problem framing that uses elements of operational art to conceive and construct an operational approach to solve identified problems. Commanders and their staffs use Army design methodology to assist them with the conceptual aspects of planning.Here is a hypothetical sequence diagram for a troop level operation to seize an objective. It is simplistic but it is a demonstration.

![](/images/1SKI8UA5JIrG1wtjM-Ic1rA.png)

The down and dirty on notations:

* Each of your entities are listed across the top of the diagram, this could be any independently operating entity on the battlefield. Units (A Troop), resources (Humanitarian Aid), key personnel (commander, CSM, S3).
* Each entity has a dashed line running vertically below it termed the life line. The life line extends for as long as the entity is alive. If the entity ceases to exist stop the life line and put an X at the bottom. Examples of this would be when your air support goes off station, or you have expended all of a particular resource like mines.
* Draw arrows between your life lines to show messages being passed between entities, such as giving orders or providing a status update. Messages are passed in sequence from top to bottom on the diagram.
* A solid line with a solid arrow is a synchronous message, meaning that the caller is going to wait for the recipient to respond before taking further action.
* A sold line with an open arrow is an asynchronous message, meaning that the caller is not going to wait for the recipient to respond before taking its next action.
* Dashed lines are response messages which could be notification of task completion, a reconnaissance report, a LACE report.
* Blocks over a life line show that the entity is currently busy. So if a platoon is ordered to conduct an assault, the platoon’s life line should be blocked until they have seized the objective.
* Entities can send messages to themselves if you want to show what a unit is doing internally to complete a higher unit’s order.
The advantage is that you end up with a quick visual guide to the sequence of operations as planned. A great companion to the operations overlay and allow a leaders to see the whole event.

There are probably a few disadvantages as well. More than likely they include:

* Do you need another MDMP product? If you feels it adds value to your operation go for it. The great thing about UML is that you only need to use the artifacts that help you design. But I recognize that now keeping your operational graphics, narrative, timeline, and coordinating instructions is a huge pain.
* They can become very wide, which can make them a little unwieldy to print.
* The diagram doesn’t have a great mechanism for dealing with branch or contingency plans. If you really need to deal with serious branches, start a second diagram.
  