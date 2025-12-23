# Packing information into names

## key idea
- Pack your information into your names
- think name as a tiny comment

### Choose Specific Names
```javascript
/// Bad example
const getPage = () => {}

///Good one
const fetchPage = () => {}
```
as you see example above, if you want to get page from internet, the word "get" is too ambiguous, so better avoid those ambiguous names

### Finding More "Colorful" Words
- use thesaurus or ask someone to find a proper words 
    
    *thesaurus is a dictionary to find synonyms

the below is example of word list

| Word  | Alternative |
|-------|-------------|
| send  | deliver, dispatch, announce, distribute, route |
| find  | search, extract, locate, recover |
| start | launch, create, begin, open |
| make  | create, set up, build, generate, compose, add, new |

#### It's better to be clear and precise than cute

### Avoid Generic Names like tmp and retval
- generally tmp or retval doesn't pack much information

but the below case is totally fine as the tmp is literally temporal storage.
```javascript

if (a > b) {
 let tmp = a;
 a = b;
 b = tmp;
}

```
#### The tmp should be used only in cases when being short-lived and temporary is the most important fact about that variable.

### Loop Iterators
