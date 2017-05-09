The happy middle ground, jOOQ.

+++

In terms of solving the second problem, jOOQ looks pretty much exactly like Hibernate with the addition that it
also lets you write your own mappers if you want to go that route.

+++

It's the way that jOOQ solves the second problem that sets it apart from the competition.

jOOQ at its core, is a DSL for generating type safe parameterized SQL queries.

This means no more String concatenation to build up your queries.

+++

Additionally because the DSL is designed to mirror as closely as possible the generated SQL, it also means it's
possible in jOOQ to represent (nearly) any valid SQL expression and to do so in a safe manner that's checked
for consistency and correctness at compile time.

+++

jOOQ also comes with optional tooling to perform code generation to do things like generate enums for table and
column names, or DTOs and DAOs for performing DB operations.

+++

It's possible to simply use Strings for your column and table names, but using the generated enums allows for the
compiler to enforce constraints such as verifying that a column actually exists on the table that's being queried
against.

+++

Lastly, if you want to take things a step further, much like Hibernate jOOQ allows for a code first approach
that can generate a DB Schema from your DTOs.

+++

The real win with jOOQ is that it's a flexible collection of utilities that allows each team to use only the pieces
that make sense for their project and their particular use case.