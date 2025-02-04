# Bug - References not updated if wrapped within a list

This is a replication of a bug where references are not updated if they are wrapped within a list.

To observe the bug:

1. Run `pnpm install`
2. Run `pnpm dev`
3. Go to http://localhost:3000/admin/index.html#/collections/author/~
4. Delete `content/authors/napoleon.md`
5. You will see that the reference to `napoleon.md` remains in `content/posts/learning-about-markdown.mdx`, whereas it has been correctly removed from `content/posts/learning-to-blog.mdx`

The schema change that makes this fault apparent is [here](https://github.com/ncn-ssw/ref-integrity-bug/commit/1d2cb2a94dace4dede57982d83fbb7e744b3718c)

## LICENSE

Licensed under the [Apache 2.0 license](./LICENSE).
