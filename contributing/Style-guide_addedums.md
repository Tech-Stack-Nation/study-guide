# Those are my recommendations on top of the Angular Style guide:

In random order, as they pop into mind, and all are open for discussion.

* Every sample _must_ have a readme that explains at least the main goal/point for that example
  * it must be named `readme.md` and be located in the demos root.
  * the readme will be available in the demo app, next to the demo.
* Every sample _must_ be tagged for its target (beginner/immediate/advanced)
* Every sample _should_ be tagged for the group/kind
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
  * if used, ***must*** have an readme entry on _why!_
* Variable naming
  * should be sensible
  * keep all variables camelCase
* Inline arrow functions.
  * Should be used for 1-liners only.
  * Prefer assignment to a named var.
  ```typescript
  const DropOpeningSlash = (s:string) => s.startWith('/') ? s.sclice(1) : s
  ```
  * when longer as 1 line this is even more mandatory.
  * use sensible naming
* Restrict size of single files to max ~100 lines.
  * Makes it more easy to reason about it.
  * makes it way harder to put too much responsibilities into 1 component/service/pipe/gizmodo
  * 
* prettier all the things.
* eslint all the things. (we will provide some reasonable yet rigid default there)
* I'm not sure, but perhaps demand at least a unit test? But that might scare beginners of off contributing.
* for beginners, everything in a CLI monorepo. We can have multiple projects in there. (libraries/etc)
* for experts the same, but perhaps with NX/lerna? ~~Although I do have some doubts about this. (let me explain, those things are actually tooling that has little to nothing to do with Angular, although they are related)~~ 
* No CSS frameworks, only plain CSS.
  * also no deviriates. we are teaching Angular, not CSS
  * by doing this, it highlight the strong CSS separation Angular already provides.
  * a set of reasonable defaults will be provided.
  * exception for when the framework is the lesson.


All of those are _guidelines_ and can be broken when there is a compelling reason to do so. However, when one of the rules needs to be broken, this needs to be **documented** inside of the demos readme. 
