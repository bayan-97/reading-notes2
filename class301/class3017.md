# What Google Learned From Its Quest to Build the Perfect Team

*A classmate* : that some students were putting together teams for ‘‘case competitions,’’ contests in which participants proposed solutions to real-world business problems that were evaluated by judges, who awarded trophies and cash. 

*The competitions were voluntary,*
 but the work wasn’t all that different from what Rozovsky did with her study group: conducting lots of research and financial analyses, writing reports and giving presentations. 
 
 project Aristotle’s researchers 
 reviewing a half-century of academic studies looking at how teams worked. Were the best teams made up of people with similar interests? Or did it matter more whether everyone was motivated by the same kinds of rewards? Based on those studies, 
 

## our data-saturated age

enables us to examine our work habits and office quirks with a scrutiny that our cubicle-bound forebears could only dream of. Today, on corporate campuses and within 

university laboratories, psychologists, sociologists and statisticians are devoting themselves to studying everything from team composition to email patterns in order to figure out how to make employees into faster, better and more productive versions of themselves. 

The company’s top executives long believed that building the best teams meant combining the best people.

## project Aristotle’s researchers 
No matter how researchers arranged the data, though, it was almost impossible to find patterns — or any evidence that the 

composition of a team made any difference. ‘‘We looked at 180 teams from all over the company,’’ Dubey said. ‘‘We had lots of data, 

but there was nothing showing that a mix of specific personality types or skills or backgrounds made any difference. The ‘who’ part of the equation didn’t seem to matter.’’

After looking at over a hundred groups for more than a year, Project Aristotle researchers concluded that understanding and 

influencing group norms were the keys to improving Google’s teams. But Rozovsky, now a lead researcher, needed to figure out which norms mattered most. Google’s research had identified dozens of behaviors that seemed important, except that sometimes the norms of one effective team contrasted sharply with those of another equally successful group.

# How I explained REST to my brother

 1- whole world wide web is built on an architectural style called “REST”. REST provides a definition of a **“resource”**, which is what those things point to.

  web page is a “representation” of a resource. Resources are just concepts. URLs--those things that you type into the browser.

  hose URLs tell the browser that there's a concept somewhere. A browser can then go ask for a specific representation of the concept. 
  
  Specifically, the browser asks for the web page representation of the concept.
2- When Fielding and his buddies started building the web, being able to talk to any machine anywhere in the world was a primary concern. Most of the techniques we use at work to get computers to talk to each other didn't have those requirements. You just needed to talk to a small group of machines.

**Machines** don't have a universal noun - that's why they suck. Every programming language, database, or other kind of system has a different way of talking about nouns. That's why the URL is so important. It let's all of these systems tell each other about each other's nouns.

##  a machine canot understand a normal web page

because web pages are designed to be understood by people. A machine doesn't care about layout and styling. Machines basically just need the data. Ideally, every URL would have a human readable and a machine readable representation. When a machine GETs the resource, it will ask for the machine readable one. When a browser GETs a resource for a human, it will ask for the human readable one.


## ore or less, this is what engineers do in the web development world, thanks almost entirely to the popularity of RESTful web frameworks like Ruby on Rails.

But this is a very recent change! Just a few years ago, the large majority of developers were busy writing layers of complex specifications for how to access data in a different way that isn't nearly as useful or eloquent.

 Nouns weren't universal and verbs weren't polymorphic. They basically ignored throwing out decades of real field usage and proven technique and kept starting over with something that looks a lot like other systems that have failed in the past. They used HTTP but only because it let them talk to our network and security people less. It was like trading simplicity for flashy tools and wizards.





