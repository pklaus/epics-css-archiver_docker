## A Docker Distribution of BEAUTY

The [CS-Studio based RDB Channel Archiver for EPICS][css-rdb]
is an Eclipse "plugin" for CS-Studio that runs in headless mode.
It's sometimes called “Best Ever Archive Toolset, yet” (BEAUTY).

### Docker Configuration

The distribution is split into two containers:

* one container running a PostgreSQL database (`epics-css-archiver-db`), and
* another one running the archiver application (`epics-css-archiver-app`).

They need to be connected to the same docker network.

### Furhter Technical Info About BEAUTY

Technical Information:

* The two subfolders `db` and `app` contain the sources to build the docker images.
* This distribution uses the [compiled versions from SNS][sns-dist].
* The SQL files with the database schema used for setting up the PostgreSQL container
  is mostly taken from the [dbd folder of the plugin org.csstudio.archive.rdb][dbd].

Furher resources on BEAUTY:

* CS-Studio Wiki:
    * RDB Archive Basic  Info: <https://github.com/ControlSystemStudio/cs-studio/wiki/RDBArchive>
    * RDB Archive Engine Info: <https://github.com/ControlSystemStudio/cs-studio/wiki/RDBArchiveEngine>
* Old but rather complete documentation on the CS-Studio RDB Archiver: <>
* SNS CS-Studio developer documentation on the RDB Archiver with further links: <https://ics-web.sns.ornl.gov/css/devel.html#archiver>
* Source code of the relevant CS-Studio plugins:
    * org.csstudio.archive.engine <https://github.com/ControlSystemStudio/cs-studio/tree/master/applications/archive/archive-plugins/org.csstudio.archive.engine>
    * org.csstudio.archive.config <https://github.com/ControlSystemStudio/cs-studio/tree/master/applications/archive/archive-plugins/org.csstudio.archive.config>
    * org.csstudio.archive.rdb <https://github.com/ControlSystemStudio/cs-studio/tree/master/applications/archive/archive-plugins/org.csstudio.archive.rdb>

[css-rdb]: http://cs-studio.sourceforge.net/docbook/ch11.html
[dbd]: https://github.com/ControlSystemStudio/cs-studio/tree/master/applications/archive/archive-plugins/org.csstudio.archive.rdb/dbd
[sns-dist]: https://ics-web.sns.ornl.gov/css/updates/apps/?C=N;O=A
