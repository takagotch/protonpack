### protonpack
---
https://github.com/poetix/protonpack

```java
Stream<> infiniteInts = Stream.iterate(0, i -> i + 1);
Stream<Integer> finiteInts = StreamUtils.takeWhile(infiniteInts, i -> i < 10);

assertThat(finiteInts.collect(Collectors.toList()),
  hasSize(10));
  
Stream<> ints = Stream.of(1,2,3,4,5,6,7,8,9,10);
Stream<> skipped = StreamUtils.skipWhile(ints, i -> i < 4);
List<> collected = skipped.collect(Collectors.toList());
assertThat(collected,
  contains(4, 5, 6, 7, 8, 9, 10));

Stream<> streamA = Stream.of("A", "B", "C");
Stream<> streamB = Stream.of("Apple", "Banna", "Carrot", "Doughnut");

List<> zipped = StreamUtils.zip(streamA,
    streamB,
    (a, b) -> " is for " + b)
  .collect(Collectors.toList());
  
```

```
```

```
```
