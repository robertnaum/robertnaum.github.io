**Thoughts on database design**

I thought I would describe how I've evolved over the years related to database design.  When I got started, I read something about creating the "right" indexes.  I wondered what the "right" indexes were.  I started guessing what the "right" indexes were.  Soon enough, I started adding an index here, an index there, and the next thing you know I've got a bunch of indexes.  Dropping the indexes turns out to be a tougher problem than I imagined.

So, I've evolved.  I am now of the opinion that you shouldn't put any indexes at all (except primary keys/clustered indexes).  Wait a couple of weeks and see what the usage patterns are.  Then look at some queries with your favorite querying tool and see what the analytics say.  Do you have a lot of "key lookups"? If so, then you might need more non-clustered indexes.
