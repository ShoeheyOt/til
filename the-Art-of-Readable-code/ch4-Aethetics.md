# Aethetics

Good source code should be just as easy on the eyes.

- Use consistent layout, with patterns the reader can get used to.
- Make similar code look similar.
- Group related lines of code into blocks.

It's easy to work with code that's aesthetically pleasing.

```javascript
///bad example
class Calculater {
  ///this is a class to calculate input numbers
  public add (a, b){ ///and return the result
    return a + b;
  }
}

///good example
///this is a class to calculate input numbers and return the result
class Calculater {
  public add (a, b){     
    return a + b;
  }
}

```
