## The low level option, JDBC (and its cousin JDBCTemplate)

---

JDBC provides an abstraction to accept a partially parameterized SQL expression as a String and returns
the semantic equivalent of a List of Maps whos keys are column names.

---

Wait… What do you mean *partially* parameterized?

Although values to filter a query on can be parameterized, columns to be sorted on can *not* be. <!-- .element: class="fragment" -->
