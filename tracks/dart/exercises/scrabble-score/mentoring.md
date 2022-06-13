# Mentoring

## Reasonable solution
Students should get themselves familiar with [Map][reference-map-class] and how we can use its methods for our benefit.

```dart
int score([String word]) {
  var values = {
    'A': 1,
    'B': 3,
    'C': 3,
    'D': 2,
    'E': 1,
    'F': 4,
    'G': 2,
    'H': 4,
    'I': 1,
    'J': 8,
    'K': 5,
    'L': 1,
    'M': 3,
    'N': 1,
    'O': 1,
    'P': 3,
    'Q': 10,
    'R': 1,
    'S': 1,
    'T': 1,
    'U': 1,
    'V': 4,
    'W': 4,
    'X': 8,
    'Y': 4,
    'Z': 10,
  };

  return word
      .toUpperCase()
      .split("")
      .fold(0, (prev, curr) => prev + values[curr]);
}
```

## Common suggestions
- They should use [MAP][reference-map-class] and get familiar with it. Some exercises will be easier for the students using it.
- [fold-method][reference-fold-method] is very useful for future challenges. Make sure they understand how it works
- If they get stuck, just refer them to [this][reference-youtube-video] YouTube tutorial to solve this exercise.


[reference-map-class]: https://api.dart.dev/stable/2.10.4/dart-core/Map-class.html
[reference-fold-method]: https://api.dart.dev/stable/1.10.1/dart-core/List/fold.html
[reference-youtube-video]: https://www.youtube.com/watch?v=myMQCtk7U30
