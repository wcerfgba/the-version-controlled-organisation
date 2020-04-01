# The Version Controlled Forum

This application implements a simple forum system with support for nested categories and flat-threaded topics.

When installing this app, create a directory for each category a forum topic can live in. Provide a description of each category here.

To create a new topic, copy the provided `_Topic.md` template into the appropriate category and rename it to match your topic title, and write the opening post.

To reply to a topic, append a newline to the end of the file, followed by a horizontal rule with `---`, and write your reply below this divider.

When reading topics in the forum, it is not necessary to sign posts because this information can be made visible using `git blame`, or by using `git log --reverse --format="%n# %aD | %aN | %h" -p`.