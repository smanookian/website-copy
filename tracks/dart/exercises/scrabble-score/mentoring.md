# Mentoring

## Reasonable solutions

There are two ways to solve this exercise. Students should learn about both methods if possible, but you can chose either one of them.
Most importantly let them get familiar with the Map class and how it works.

### Using the fold-method
```dart
int score(String word) {
  Map<String, int> letterValues = {
    "a": 1, "b": 3, "c": 3, "d": 2, "e": 1,
    "f": 4, "g": 2, "h": 4, "i": 1, "j": 8,
    "k": 5, "l": 1, "m": 3, "n": 1, "o": 1,
    "p": 3, "q": 10, "r": 1, "s": 1, "t": 1,
    "u": 1, "v": 4, "w": 4, "x": 8, "y": 4,
    "z": 10
  };
  return word.toLowerCase().split('').fold(0, (previous, current) => previous + letterValues[current]);
}
```

### Using map- and reduce-methods
```dart
int score(String word) {
  Map<String, int> letterValues = {
    "a": 1, "b": 3, "c": 3, "d": 2, "e": 1,
    "f": 4, "g": 2, "h": 4, "i": 1, "j": 8,
    "k": 5, "l": 1, "m": 3, "n": 1, "o": 1,
    "p": 3, "q": 10, "r": 1, "s": 1, "t": 1,
    "u": 1, "v": 4, "w": 4, "x": 8, "y": 4,
    "z": 10
  };
  return word.toLowerCase().split('').map((x) => letterValues[x]!).reduce((previous, current) => previous + current); 
}
```

## Common suggestions

- The best solution is the one with [fold-method][reference-fold-method], because students will use this in the future often.
- Get familiar with the [Map class][reference-map-class]
- You can show them [map method][reference-map-method] and [reduce method][reference-reduce-method] as a plus

[reference-map-class]: https://api.dart.dev/stable/2.10.4/dart-core/Map-class.html
[reference-fold-method]: https://api.dart.dev/stable/1.10.1/dart-core/List/fold.html
[reference-map-method]: https://api.dart.dev/stable/2.9.1/dart-core/Iterable/map.html
[reference-reduce-method]: https://api.dart.dev/stable/2.14.4/dart-core/Iterable/reduce.html

## Solution explanation video

Forward them to this [YouTube video][reference-youtube] to have a step by step solution

[reference-youtube]: https://www.youtube.com/watch?v=myMQCtk7U30
