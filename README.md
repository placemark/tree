# tree

Build and manipulate trees.

Basically, I've implemented a lot of tree structures that are then serialized
into a database. Even if you're using a document database, you probably aren't going
to store the whole tree as a single document, but instead use links to point to a node's
parents. That's how it usually works: there's a `parentId` column in a table and that
references another table, or even the same table, with a foreign key.

Then, you – if you're loading the whole tree from the database – rework this structure
into a nested tree that's easy to code with. This module is trying to make it easier
to do that. It's what Placemark uses, currently, for [Folder support](https://www.placemark.io/post/folders).

## Install

This package is [`@placemarkio/tree`](https://www.npmjs.com/package/@placemarkio/tree)
