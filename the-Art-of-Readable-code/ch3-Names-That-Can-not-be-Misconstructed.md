## Names That can't be Misconstructed

### Key Idea

#### Actively asking yourself once again, "What other meaning could someone think with this name?"

For example, `filter()` the word itself is ambiguous. It is unclear whether the meaning is "to pick out" or "to get rid of". If you want to pick out, it is better using `select`, if you want to get rid of, it is better using `exclude` instead.

Another example is the word `limit`. It can be inclusive or exclusive. Instead, it is better use `min_` or `max_` prefix in order to avoid drawing an unnecessary attention.
Same idea, the word `stop` is misleading word, it can be whether "up to" or "up to and including". Alternatively, you can use `last` and `end` for "up to and including".

#### Naming Booleans

when variables come to boolean, it should be clear as well.

`const readPassword = true;`

This example is dangerous because it can be whether "We need to read a password" or "The password has already been read".This case, you should not use the word "read", you can name it as `needPassword` or `isAuthenticated` instead.
For boolean variable, you can use `is`, `has`, `can` or `should` in order to make the variable clear.

Finally, it is better to avoid using negated terms in name. For example, `const isUnauthenticated = false;` you should use `const isAuthenticated = true;` for readability.

### Matching Expectation of Users

Beware of users' expectations about certain words. For example, users may expect `get()` or `size()` to be lightweight methods.
