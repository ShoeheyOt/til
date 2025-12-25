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
    
    thesaurus is a dictionary to find synonyms

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
- i, j, k for indicator is ok, but make sure it is easy to trace.

```javascript
for (let i = 0; i < clubs.size; i++){
    for (let j = 0; j < clubs[i].members.size(); j++){
        for (let k = 0; k < users.size(); k++){
            if ( clubs[i].members[k] == users[j])
            console.log(`user ${users[j]} is in club ${clubs[i]}`);
        }
    }
}
```
the example above doesn't work as k and j indicators in if statement are reversed and it is not easy to find the bug until you run the codes.

`if(clubs[i].members[k] == users[j])`

so in order to avoid it, it is better to use more precise names like (club_i, members_i, users_i) or (ci, mi, ui) for short.

`if(clubs[ci].members[ui] == users[mi]) /// easy to find a bug`

`if(clubs[ci].members[mi] == users[ui]) /// now bug fixed`

### Attaching Extra Information to a Name

#### if there is a important information about variables that readers must know, it's worth attaching word to variable name.

for example

`const id = "af84ef845ca3`

you might want to add information that the variable id above is hex code so they would understand what kind of information is stored instantly.

`const hex_id = "af84ef845ca3"`

### Values with Units

#### Same idea as above, you want to add unit to variable so that readers would not get confused.

`const size = 5 ///It is easy to misunderstand it can be length, byte and so on`

`const size_mb = 5 /// now it is obvious`

### Encoding Other Important Attributes

sometime you want to add extra information into variables.

 `unsafeInput /// not yet safe user input`
 
 `safeInput /// after checking user input`

#### But be careful adding these attrubutes might be redundant. use them when it is easy to be misunderstood.

## How Long Should a Name Be?

The longer name is harder to remember and need more space, so you can use short (or even a single letter) name as a variable.
This is trade off.

### Shorter Name Are Okey for Shorter Scope
Identifiers or functions that have a smal scope don't need to carry as much information. This is the timing you can use and name a shorter variable. The point is how many other lines you need to use this variable.

### Acronyms and Abbreviations

#### The most important rule here is "Would a new teammate understand what the name means?"
project-specific abbreviations are usualy a bad idea. They are unfamiliar to the people outside of the project, and need more time for new member to understand the codes.
