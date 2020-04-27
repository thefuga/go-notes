# Good practices
## Formatting

- Formatting should be performed by `gofmt`.

## Comments

- Packages should have a top block comment for documentation - multi file packages should only have one comment.
- Comments are plain text, no annotations for formatting is needed.
- Comments preceding top-level declarations are used for documentation. Every exported name should have a doc comment.

    ```go
    // Foo is an example of how doc comments should be.
    func Foo() {
    	return "foo"
    }
    ```

- Related constants or variables may have only one comment to introduce them.

    ```go
    // Dimentions of something.
    var(
    	length uint32
    	width uint32
    )
    ```

## Names

Names have a semantic effect in Go. So naming is very important.

- Go uses cammelCase and PascalCase to multiword names.
- Names preceded with upper case are exported.

#### Packages

- Package names should refer to it's content. They should be short, concise and evocative. Package names MUST:
    - Have one word.
    - Be lower case.
    - NOT have mixedCase or under_scores.

#### Getters and setters

- Getters and setters may be used when necessary.
- Getters should not take the prefix `get` . If there's a field `name` it's getter must be called `Name` .
- Setters should take the prefix `set`. If there's a field `name` it's setter must be called `SetName` .

#### Interfaces

- One-method interfaces should be named with the method's name followed by the suffix `er` . E.g. `Reader` , `Writer` .
- Well-known method's names such as `Read` , `Write` , `Flush`, `Close`, should only be used if they have the same signature and meaning. E.g. a string converter should be called `String` not `ToString`.

## Arrays and Slices

- Array pointers like `array *[10]float64` are not idiomatic and should be avoided. Slices should be used instead.


# Style guides
## Links
- [uber-go/guide](https://github.com/uber-go/guide/blob/master/style.md)
- [sourcegraph/thesrc](https://github.com/sourcegraph/thesrc)
- [What's in a name?](https://talks.golang.org/2014/names.slide)
- [golang/go](https://github.com/golang/go/wiki/CodeReviewComments)
- [Thanos](https://thanos.io/contributing/coding-style-guide.md/)
- [Go DDD](https://github.com/marcusolsson/goddd)

# Reading
## Links
- [golang/go](https://github.com/golang/go/wiki)
- [Effective Go](https://golang.org/doc/effective_go.html)
- [Writing Web Applications](https://golang.org/doc/articles/wiki/)
- [Introduction](https://astaxie.gitbooks.io/build-web-application-with-golang/en/)
- [Learn Web Programming in Go by Examples](https://gowebexamples.com)
- [Go by Example](https://gobyexample.com/)
- [golang/go](https://github.com/golang/go/wiki/CodeReviewComments)
- [Learn Go reflections and generic designs with a practical example](https://www.freecodecamp.org/news/a-practical-example-go-reflections-and-generic-designs-4868b6cdb2dc/)
- [Less is exponentially more](https://commandcenter.blogspot.com/2012/06/less-is-exponentially-more.html)
- [SOLID Go Design](https://dave.cheney.net/2016/08/20/solid-go-design)
- [Self-referential functions and the design of options](https://commandcenter.blogspot.com/2014/01/self-referential-functions-and-design.html)
- [Functional options for friendly APIs](https://dave.cheney.net/2014/10/17/functional-options-for-friendly-apis)
- [Advanced Go Concurrency](https://encore.dev/blog/advanced-go-concurrency)

# Videos
## Talks
- [How I Built Microservices In Go In 30 Minutes](https://www.youtube.com/watch?v=bM6N-vgPlyQ)
- [Why Go Is Successful (aka Simplicity is Complicated)](https://www.youtube.com/watch?v=k9Zbuuo51go&t=8s)
- [Concurrency Patterns In Go](https://www.youtube.com/watch?v=YEKjSzIwAdA)
- [Writing Beautiful Packages in Go](https://www.youtube.com/watch?v=cmkKxNN7cs4)
- [Simulating A Real-World System (Coffee Shop) In Go](https://www.youtube.com/watch?v=jJS6G7irZSc&t=1s)
- [Self Deploying Go Applications](https://www.youtube.com/watch?v=SmtDEhuDQy4)
- [How Do You Structure Your Go Apps?](https://www.youtube.com/watch?v=1rxDzs0zgcE)
- [Advanced Topics in Programming Languages: Concurrency/message passing Newsqueak](https://www.youtube.com/watch?v=hB05UFqOtFA)
- [Go In 5 Minutes - Short, helpful screencasts for professional Go developers](https://www.goin5minutes.com/)
