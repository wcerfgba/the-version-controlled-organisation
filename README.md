# The Version Controlled Organisation

A Git workflow for modern organisations.

## Manage my organisation with Git? Are you serious?

Yes, I am completely serious. 😊 Git -- and the tooling around it -- is capable of providing a simple and complete information infrastructure which can work for many organisations.

Most organisations need at least some of the following things:

* A place to put documents -- authoritative descriptions of business processes, customer portfolios, proposals, receipts, graphics, code, ...
* A way to structure documents -- to keep everything organised
* A shared calendar -- for meetings and events
* A shared task list, workflow management, or project management system -- to organise work, people, processes and resources so everyone knows what they need to do, and so we can ensure we are achieving our goals
* A forum -- somewhere to discuss ideas and vote on proposals [1]

By starting with a few basic processes in the form of this repo, you can use Git to fulfil all of these needs.

The author's primary assumption is that any information necessary for an organisation to function -- goals, processes, coordination, day-to-day communication, ... -- can be communicated by words and diagrams alone. [2] If this is true then it should be possible to manage an organisation using contemporary computing machinery (hardware and software), although providing an ergonomic implementation with simple semantics which achieves all functional requirements seems like it would be quite challenging...

Fortunately, Git can provide us with a very strong foundation. Here's how:

* **Files = Documents** - Text files like this can capture everything I can think except for possibly diagrams/pictures and music, and for these media we have many filetypes at our disposal. If it's pertinent informtion, I can put it in a computer file.

* **Searchable Hierarchy** - Directories nest into a tree, which if we are careful to structure properly, makes it very easy to know where information should live (self-defining) and makes it easy to navigate all information available (self-indexing). If we keep information in suitable filetypes for our organisation -- we are using Git so plain text files should be our default -- then we can search all of our documents very easily, so it becomes very hard to lose things.

* **Unified** - If we keep all information as files in a single repo, then all of your organisation's information is in one place. Have you ever wondered where the 'file' for your Google Calendar lives, or how it's structured, how you could search or export the information inside? What about your contacts, emails, support tickets, product epics, and customer portfolios? If you bring all of that data into a single platform, you can search everything, cross-reference anything with anything else, using a single set of tools, and this can give you superpowers. 🦸

* **Changes = Notifications + Provenance + Confidence** - Changes to files in the repo happen in the form of commits, which include an author and a message. Every time you download updates ("pull the repo"), you get a list of all the updates to every scrap of information in your organisation: new work in your inbox, meeting time changed, some replies to a query you opened, all listed cleanly in the repo history. The history-like nature of the Git log brings about the wiki effect, allowing us to reverse breaking changes easily, which empowers people to be bold and make changes in the first place, which propotes innovation, iteration, and moving fast.


## How to use this repo

In addition to this document detailing the concept of the Version Controlled Organization, this repo also provides working implementations of various 'applications'. An application in the VCO sense is a directory structure and files which can be used to manage a particular type of information in a particular way. Application templates live in the `_Apps` directory. In order to use an application, you should 'install' it by copying the template directory and its contents into another location in the repo, and then you can make changes within this 'instance' of the application.

Applications work on a "trunk-based development"-style workflow: changes should be merged into master as soon as possible and everyone should pull master frequently, so everybody stays as close to master as possible. So long as you do not force-push, it is safe to work with most applications by committing straight to master and pushing master: if you do something wrong, someone will quickly notice, let you know [3] and revert the change. 

The remaining files in this repo provide an example of a Version Controlled Organisation on the theme of a modern SaaS startup, VCOCorp. Each top-level directory corresponds to a department at VCOCorp, and provides a workspace for apps and files for each department to use internally. We also have the top-level `Company` directory for company-wide applications and files -- this is where we share events and notifications that everyone should see, regardless of their department.

Our central hub and 'home page' is the index README file in the Company workspace at `Company/README.md`, this would be a good document to visit next.


## Contributing

Your feedback and contributions to this project are greatly appreciated. PRs, issues and forks welcome! 💜 


## Notes

[1] Many organisations do not have a formal or obvious forum for shop-talk, and many discussions happen around watercoolers, in meetings, and in private email threads / Slack DMs, which might otherwise be beneficial for an organisation to instead take place in a transparent, long-form, and asynchronous way. Just like this document you are reading now. 😉

[2] OK, I am stretching this a bit here, because the bandwidth for emotional communication can become much narrower with just text. Even a HD video call lacks nuances in body language and voice which form part of our connection to other people and the 'humanness' of our interaction. Any remote organisation with a healthy culture should promote high bandwidth social communication -- imagine if you and your manager never had a 1:1 call! 

That said I do think shop-talk can be contained within a more prescribed boundary. Perhaps we should say any 'operational' information?

[3] This example illustrates an example of an organisational communication use case which is not well-met by Git or VCO, which is real-time signalling. VCO is best supplemented with additional channels for real-time communication.

## Bibliography

* git-bug -- https://github.com/MichaelMure/git-bug
* GitLab Handbook Usage -- <https://about.gitlab.com/handbook/handbook-usage/>
* Rust RFCs -- <https://github.com/rust-lang/rfcs>