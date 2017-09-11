# Language Todo.TXT Plus - Syntax highlighting for Todo.TXT

This is for comfort work with Todo.TXT-formatted `*.txt` files.

If you don't know anything about Todo.TXT, go to [TodoTXT.com](http://todotxt.com) and read all about it! It's worth it. :smile:


## Features

- Support of Ukrainian & Russian symbols
- Add **comments**, **failed tasks**, **bold** & **italic** emphasis, **raw**, **strikethrough**
- Projects, contexts and extensions can contain only letters and dashes: `foo-bar:goo-moo @foo-bar +goo-moo`
- Support of indentation

  ```TodoTXT
  foo bar @Monaco
    goo doo +zoo
  ```


## Very Quick Usage Guide

Syntax        | Description     | Example
---           | ---             | ---
`~~...~~`     | Strikethrough   | `~~foo bar~~`
`**...**`     | Bold (strong)   | `bar **foo** goo`
`_..._`       | italic (emphasis) | `bar _foo_ goo`
`- ...`       | Failed task     | `- foo bar task @prj`
`x ...`       | Completed task  | `x foo bar +task`
`+{prj-name}` | Project         | `+foo-bar`, `+'foo bar'`
`@{context}`  | Context         | `@foo-bar`, `@'foo bar'`
`{param}:{value}` | Extension   | `some-param:some-value`, `param:'some value'`
`t:{yyyy-mm-dd}` | Date, way 1  | `foo t:2017-07-06 bar` 
`{yyyy-mm-dd}` | Date, way 2    | `foo 2017-07-06 bar`
`{hh-mm}`     | Time date       | `11-30`
`{hh-mm-hh-mm}` | Time date period | `11-30-12-30`
`due:{yyyy-mm-dd}` | Due to date | `foo due:2017-07-06 bar`
`(A-Z) ...`   | Priority        | `(A) foo @bar goo` 
~             | ~               | `(B) goo @joo noo`
`... # ...`   | Comments        | ` foo  # bar`

Also, you can use **inline raw code**:

```
foo `bar goo` hoo
```



## Big Example

```TodoTXT
(A) buy **milk** @house-tasks +im-good-man
(Z) fix ~~the chair~~ the table @house-tasks
(B) _go for a walk_ with dog +im-good-man

do some big project +project-name due:2017-12-31
  some part of the project @important
    deeper indention @too-deep
  another **part** of the project, with code `int main()`
  x completed part of +project-name
  - failed part
  
2017-07-06 this is another task with some-param:some-value
x 2017-06-01 2016-05-21 due:2017-08-31 some ended task with ending date
```



## What To Do If Syntax Highlight Doesn't Work Properly?

If it doesn't work properly out of box, that's maybe because your current syntax theme doesn't use same CSS identifiers, as declared in this plugin. So, try to init them manually. Open `styles.less` and add something like this:

```less
// your color for italic (emphasis): `_..._`
span.syntax--markup.syntax--italic {
  color: #ccc;
}
// your color for raw code
span.syntax--markup.syntax--code {
  color: #ddd;
}
// your color for bold (strong): `**...**`
span.syntax--markup.syntax--bold {
  color: #aaa;
}
// your color for strikethrought: `~~...~~`
span.syntax--markup.syntax--strike {
  color: #bbb;
}
// your color for context: `@...`
span.syntax--todotxt.syntax--context {
  color: #ddd;
}
// your color for project: `+...`
span.syntax--todotxt.syntax--project {
  color: #ddd;
}
// your color for extension: `foo:bar`
span.syntax--todotxt.syntax--extension {
  color: #ddd;
}
// your color for date: `yyyy-mm-dd`
span.syntax--todotxt.syntax--date {
  color: #ddd;
}
// your color for priority: `([A-Z]) ...`
span.syntax--todotxt.syntax--priority {
  color: #ddd;
}
```

You can init or override only selectors you need.



## Support

For more info, write me: `git.lerbigdev at gmail.com`

With best regards, your LerDev :smile:
