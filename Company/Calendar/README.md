# The Version Controlled Calendar

We present one way to manage a calendar via a Git repository.

Each calendar date exists as a folder like `Calendar/2020/03-March/29-Sunday`. Inside each date we can add each event as a (Markdown) file, with the start and end times in the filename, like `1730_1800_My_Example_Event.md`.

## Creating calendar folders

You can prepopulate the directory hierarchy for a calendar to suit your preferences. The structure described at the beginning of this document can be generated with the following bash commands:
```
for i in {0..365}; do                                                      
  mkdir -p $(date +"%Y/%m-%B/%d-%A" -d "+$i days")
done
```
This generates 365 days of calendar day folders starting from the current date. Once you install this app you can always change the format and this documentation to suit your own needs. 😊

## Listing calendar events

It gets a bit noisy if you have lots of potentially empty folders. You can use the `tree` command with `--prune` to get a nicely indented list of events without empty dates in your way:
```
% tree --prune Calendar
Calendar
├── _0000_0000_Event.md
├── 2020
│   └── 03-March
│       └── 29-Sunday
│           └── 1730_1800_My_Example_Event.md
└── README.md

3 directories, 3 files
```

## Repeating events

TODO