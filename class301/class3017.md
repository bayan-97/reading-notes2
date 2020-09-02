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


# APIs

An application programming interface (API) is a computing interface which defines interactions between multiple software intermediaries.

 It defines the kinds of calls or requests that can be made, how to make them, the data formats that should be used, the conventions to follow, etc. It can also provide extension mechanisms so that users can extend existing functionality in various ways and to varying degrees.
 
  An API can be entirely custom, specific to a component, or it can be designed based on an industry-standard to ensure interoperability. 
  
  Through information hiding, APIs enable modular programming, which allows users to use the interface independently of the implementation.

  ## Purpose

  In building applications, an API (application programming interface) simplifies programming by abstracting the underlying implementation and only exposing objects or actions the developer needs. 
  
  While a graphical interface for an email client might provide a user with a button that performs all the steps for fetching and highlighting new emails, an API for file input/output might give the developer a function that copies a file from one location to another without requiring that the developer understand the file system operations occurring behind the scenes.

  ## Operating systems
  

An API can specify the interface between an application and the operating system. for example, specifies a set of common APIs that aim to enable an application written for a POSIX conformant operating system to be compiled for another POSIX conformant operating system.

Linux and Berkeley Software Distribution are examples of operating systems that implement the POSIX APIs.

Microsoft has shown a strong commitment to a backward-compatible API, particularly within its Windows API (Win32) library, so older applications may run on newer versions of Windows using an executable-specific setting called "Compatibility Mode".

An API differs from an application binary interface (ABI) in that an API is source code based while an ABI is binary based. For instance, POSIX provides APIs while the Linux Standard Base provides an ABI.

## Remote APIs

Remote APIs allow developers to manipulate remote resources through protocols, specific standards for communication that allow different technologies to work together, regardless of language or platform. 

For example, the Java Database Connectivity API allows developers to query many different types of databases with the same set of functions, while the Java remote method invocation API uses the Java Remote Method Protocol to allow invocation of functions that operate remotely, but appear local to the developer

Therefore, remote APIs are useful in maintaining the object abstraction in object-oriented programming; a method call, executed locally on a proxy object, invokes the corresponding method on the remote object, using the remoting protocol, and acquires the result to be used locally as a return value.

A modification on the proxy object also will result in a corresponding modification on the remote object.

![](https://imgs.developpaper.com/imgs/2899688687-5d07315980597_articlex.png)
