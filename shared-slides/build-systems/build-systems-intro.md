## The build "life cycle"
#### (Not to be confused with the system development life cycle (SDLC))

The process of creating *tested deployable software artifacts*
<br/>
from *source* code

May include, depending on the system specifics:
* *Source code manipulation* and generation
* Source code *quality assurance*
* *Dependency management*
* *Compilation*, linking
* Binary *quality assurance*
* *Binary manipulation*
* *Test execution*
* Test *quality assurance* (e.g., coverage)
* API *documentation*
* *Packaging*
* *Delivery*
* *Deployment*

---

## Build automation

Automation of the build lifecycle

* In principle, the lifecycle could be executed manually
* In reality *time is precious* and *repetition is boring*

$\Rightarrow$ Create software that automates the building of some software!

* All those concerns that hold for software creation hold for build systems creation...

---

## Build automation: basics and styles

**Imperative**/**Custom**: write a script that tells the system what to do to get
from code to artifacts
* *Examples*: make, cmake, Apache Ant
* *Abstraction gap*: verbose, repetitive
* Configuration (*declarative*) and actionable (*imperative*) logics *mixed* together
* Highly *configurable* and *flexible*
* Difficult to *adapt* and *port* across projects

**Declarative**/**Standard**: adhere to some convention, customizing some settings
* *Examples*: Apache Maven, Python Poetry
* Separation between *what* to do and *how* to do it
  * The build system decides how to do the stuff
* Easy to *adapt* and *port* across projects
* *Configuration limited* by the provided options

---

## Hybrid automators

Create a *declarative infrastructure* upon an *imperative basis*, and
*allow easy access to the underlying machinery*

**DSL**s are helpful in this context: they can "hide" imperativity without ruling it out

Still, many challenges remain open:
* How to reuse the build logic?
    * within a project, and among projects
* How to structure multiple logical and interdependent parts?
