# Those are my recommendations on top of the Angular Style guide:

In random order, as they pop into mind, and all are open for discussion.

* Every sample _must_ have a (small) readme that explains at least the main goal/point for that example
* Every sample should be in its own lazy-loaded route. 
  * create with `npx ng generate module mySampleName --routing mySampleRoute --module app`
  * Makes it easy to read/reason about the sample
  * clears out eventual dependencies
  * keeps rebuild time low, when working on something
* inputs and outputs should be limited to max 5 total.
  * When there are more, the component at had has too many responsibilities
  * exceptions are possible, but _not without documenting the **why**_  
* same for DI, do not inject more than 5 things. 
  * when needing more, consider a service that aggregates it into 1 service
* 3trh party libs
  * must be lazy-loaded.
  * must be retained to the module that needs it.
  * should not be used at all if possible!
  * if used, ***must*** have an readme on _why!_
* prettier all the things.
* eslint all the things. (we will provide some reasonable yet rigid default there)
* I'm not sure, but perhaps demand at least a unit test? But that might scare beginners of off contributing.
* for beginners, everything in a CLI monorepo. We can have multiple projects in there. (libraries/etc)
* for experts the same, but perhaps with NX/lerna? ~~Although I do have some doubts about this. (let me explain, those things are actually tooling that has little to nothing to do with Angular, although they are related)~~ 
