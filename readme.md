# User Support System Analysis

Data that goes with ["Understanding user support systems in open source"](link), an analysis of user support systems in open source.

I used BigQuery’s [GitHub data set](https://cloud.google.com/bigquery/public-data/github) to pull a list of top open source projects (public + OSS license detected) on GitHub, by most issues opened in the most recent year (8/29/17-8/29/18). Of these, I removed a bunch of noisy data to end up with a “top 100” list.

Some criteria for how I cleaned up the data:
* Only looked at projects with >2 contributors
* Only looked at software projects (not content)
* Only looked at English-speaking projects, so I could understand them for the analysis
* Archived repositories were removed
* Mirrors of other issue trackers were removed
* Junk repositories and personal projects were removed

After getting a top 100 list, I went through each project and collected data about their support systems. This information was collected and recorded between September 5th-10th, 2018.

Some information on criteria and caveats:
* I only included a channel if the project officially named it as a *support* channel. Ex. A project might have a mailing list, but if it's used for general chatter, I didn't count it.
* Dedicated security channels (like HackerOne, or an email address) weren't included, as they're a specialized form of support
* An absolute count of support channels doesn't reflect the relative use and popularity of those channels. Ex. A project might list Stack Overflow and Gitter as channels, but hardly ever use the latter. I still counted both.
* `async_count` includes `gh_issues`
* `mailing_list` includes mailing list groups (like Google Groups and groups.io)

Special thanks to [Raúl Kripalani](https://github.com/raulk) for the BigQuery help.

Feedback or questions can be directed to [@nayafia](https://twitter.com/nayafia)

# Contributing

I don't plan to update or change this data set. If you'd like to add more data however, or if you spot any errors, feel free to open a [pull request](link).

# License and attribution

This data is available under the [Creative Commons CC0 1.0 License](https://creativecommons.org/publicdomain/zero/1.0/), meaning you are free to use it for any purpose, commercial or non-commercial, without any attribution back to me (public domain). If you do use it, I'd love to hear about it! (Find me here: [@nayafia](https://twitter.com/nayafia)) But you are in no way required to do so.
