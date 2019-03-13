# TODO How to work on this repo

# About markdown (the format of questions and answers)

[Markdown](https://daringfireball.net/projects/markdown/) is a lightweight plain textual format to author documents.
You can have:
-   Sections
-   Code blocks
-   Tables
-   Listings

Actually even this document is written using markdown.  You can
check it out for examples by opening it in your favorite text
editor.

## Some examples

A table:

| Tables   |      Are      |  Cool |
|----------|:-------------:|------:|
| col 1 is |  left-aligned | $1600 |
| col 2 is |    centered   |   $12 |
| col 3 is | right-aligned |    $1 |

A codeblock with syntax highlighting:

```java
class BestClassEver {
    public static void main(String[] args) {
        // This will get me hired for sure!!!
        System.out.println("This is a great code block");
    }
}
```

# How to check your work on localhost

All you need is a static webserver.  (One which can serve files from
a root directory.  No logic is needed for the endpoints)

One easily available solution is the HTTP server embedded in python.
It can started from the command line like this:

```sh
# For python 3
# This starts a webserver on localhost:8080
# Make sure to start it from this directory
python -m http.server 8080
```
