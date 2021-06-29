# RxJs

RxJs has a steep learning curve. To begin with, it's best to focus on a few operators and then expand from there.

If you master [map](https://www.learnrxjs.io/learn-rxjs/operators/transformation/map), [switchMap](https://www.learnrxjs.io/learn-rxjs/operators/transformation/switchmap), [filter](https://www.learnrxjs.io/learn-rxjs/operators/filtering/filter), and [take](https://www.learnrxjs.io/learn-rxjs/operators/filtering/take), you'll be on a good path. But, you'll quickly find that your project requirements will affect what you need to learn next.

As well as processing Observable streams such as [HttpClient Requests](https://angular.io/guide/http#requesting-a-typed-response), you'll need to create your own streams. Begin with [BehaviorSubjects](https://www.learnrxjs.io/learn-rxjs/subjects/behaviorsubject) - they're a natural fit for simple state management in Services.

### Rule:

- If you must subscribe to an Observable in your Component, always remember to Unsubscribe or use another method to complete the Observable before the Component is destroyed. Otherwise - memory leaks!

### Links

The Angular docs have a nice short intro to RxJs: https://angular.io/guide/rx-library

# Reactive Programming

Once you've got the hang of Observables, Reactive Programming is the next important step. Done right, it makes your Component code look simpler and it makes your application render faster.

- Use [async pipe](https://angular.io/api/common/AsyncPipe) in Container Component templates rather than subscribing in code. The [View Model pattern](https://dev.to/brandontroberts/maximizing-and-simplifying-component-views-with-ngrx-selectors-286j) simplifies this concept further.
- Use [onPush Change Detection](https://blog.angular-university.io/onpush-change-detection-how-it-works/) everywhere

### Links

- https://www.pluralsight.com/courses/rxjs-angular-reactive-development
