# Jest

Jest is a popular alternative to Karma + Jasmine. If you use Nrwl Nx, you can get it by default (but can choose Karma if you wish).

The syntax is very similar to Jasmine - more than 50% is exactly the same. If you know Jasmine, you'll immediately understand this:

```javascript
it("#getValue should return value", () => {
  const spy = jest.spyOn(someService, "getValue");
  spy.mockReturnValue("stub value");

  expect(service.getValue()).toBe("stub value");
  expect(spy).toHaveBeenCalled();
});
```

The bit where Jest really shines ahead of Jasmine (apart from speed) is Snapshot Testing. See [this article for an intro to Snapshot Testing](https://izifortune.com/snapshot-testing-angular-applications/)

### Links

- The official [docs for Jest](https://jestjs.io/)
- Some Angular [Jest Unit Test Examples](https://allenhwkim.medium.com/angular5-jest-unit-test-examples-a9538ece6cd)
- A video on [writing Angular unit tests](https://www.youtube.com/watch?v=PdVerlfmO6M)
- Advice on [changing Jasmine test syntax to Jest](https://nx.dev/latest/angular/modern-angular/karma-to-jest#3-migrate-spec-files-to-jest)

### Related

- [Testing with Karma + Jasmine](testing.md)
