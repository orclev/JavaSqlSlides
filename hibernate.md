The (_really_) high level option, Hibernate.

+++

Good news, Hibernate solves both our problems!

… and also creates new ones. <!-- .element: class="fragment" -->

+++

The process of mapping from a Record to an Object in Hibernate is actually a pretty good one. In fact almost all
solutions to this particular problem that don't involve manually writing mappers end up looking pretty much
exactly like how Hibernate implements this, namely mapping by naming convention and/or using annotations.

+++

Unfortunately in solving the **first** problem Hibernate introduces a new abstraction, HQL which obscures important
performance considerations around query construction.

+++

Compounding its sins Hibernate also abstracts away the handling of table joins, the single most performance critical
aspect of query writing.

+++

Lastly, to add insult to injury Hibernate also conflates record mapping with query construction by using DTOs to
document table relationships via the use of `@OneToMany` and `@ManyToMany` annotations.