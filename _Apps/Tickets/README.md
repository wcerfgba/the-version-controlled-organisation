# The Version Controlled Ticket System

We present a way to manage items of 'work' such as tasks, stories, support requests, RFCs, sales leads, ... using a ticketing system implemented in Git.

Our system is based around the idea of tickets and inboxes. A ticket is a Markdown file, which may conform to a template, which represents some unit of work. An inbox is a directory which can contain tickets and may contain other inboxes [1] . A ticket can only be in a single inbox at each point in time.

When you install this application, you will need to design and document your inboxes to fit your specific needs and workflow. To get you started, we present a simple three-step workflow with a single template. New tasks are created in `Todo`. When someone starts work on a task, they move the ticket to `In_Progress` [2] . As work is done on the task, people update the ticket. Once the task is 'done', the ticket can be moved to `Completed`.

[1] Inboxes may nest, but we recommend keeping the structure flat and using as few inboxes as possible.
[2] This move should be performed in a commit by itself, to ensure it shows clearly as a move in the Git log.