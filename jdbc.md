The low level option, JDBC (and its cousin JDBCTemplate)

+++

JDBC provides an abstraction to accept a partially parameterized SQL expression as a String and returns
the semantic equivalent of a List of Maps whos keys are column names.

+++

Wait… What do you mean **partially** parameterized?

Although values to filter a query on can be parameterized, columns to be sorted on can **not** be. <!-- .element: class="fragment" -->

+++

In practice this means that you still end up with a certain amount of string concatenation occuring to build up sorted
result sets.

+++

![SQL Injection](assets/this_is_how_you_get_sql_injection.jpg)

+++

Although JDBC partially solves the first problem it doesn't really do anything for the second problem.

+++

This means that it's up to each project to roll their own solution to creating mappers to translate from
`List<Map<String,?>>` to whatever POJOs they've created.

+++

JDBCTemplate (from the Spring project) provides some helpers to make this process easier, but doesn't fundamentally
change it.
