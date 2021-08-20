# Issue
It can sometimes be _frustrating as hell_ to switch to your browser from your IDE or terminal to view task requirements. It can be even more irritating when these websites don't have proper keyboard support.

To combat all this, **Issue** is a simple CLI utility for viewing GitLab project issues _(Support for GitHub, Jira, Clubhouse and more coming soon!)_.


* [Installation](https://github.com/ArjArav98/Issue/blob/master/README.md#installation)
* [Usage](https://github.com/ArjArav98/Issue/blob/master/README.md#usage)
   * [Listing Issues](https://github.com/ArjArav98/Issue/blob/master/README.md#usage)
   * [Viewing Single Issues](https://github.com/ArjArav98/Issue/blob/master/README.md#usage)
   * [Miscellaneous](https://github.com/ArjArav98/Issue/blob/master/README.md#usage)
   * [Listings Search Parameters](https://github.com/ArjArav98/Issue/blob/master/README.md#usage)
* [Potential Contributions](https://github.com/ArjArav98/Issue/blob/master/README.md#potential-contributions)
* [Tools Used](https://github.com/ArjArav98/Issue/blob/master/README.md#tools-used)

# Installation
* Download the executable corresponding to your OS from the table below.

   | OS & Architecture | Link |
   |---|---|
   |Darwin (Mac OS) AMD64| [Download](https://github.com/ArjArav98/Issue/raw/master/dist/darwin_amd64/issue) |
   |Darwin (Mac OS) ARM64| [Download](https://github.com/ArjArav98/Issue/raw/master/dist/darwin_arm64/issue) |
   |Linux 386| [Download](https://github.com/ArjArav98/Issue/raw/master/dist/linux_386/issue) |
   |Linux AMD64| [Download](https://github.com/ArjArav98/Issue/raw/master/dist/linux_amd64/issue) |
   |Linux ARM| [Download](https://github.com/ArjArav98/Issue/raw/master/dist/linux_arm/issue) |
   |Linux ARM64| [Download](https://github.com/ArjArav98/Issue/raw/master/dist/linux_arm64/issue) |
   |Windows 386| [Download](https://github.com/ArjArav98/Issue/raw/master/dist/windows_386/issue.exe) |
   |Windows AMD64| [Download](https://github.com/ArjArav98/Issue/raw/master/dist/windows_amd64/issue.exe) |

* Add the path of the directory, in which the executable is present, to your `PATH` environment variable.
* Run `issue version` to verify the successful installation!

# Usage
|Issue Listings Commands|Description|
|---|---|
|`issue list` | Lists all issues.|
|`issue list --assignee_username darth.vader69 --labels "Doing,Backend"` | Lists all issues after applying search parameters. For full list of search parameters and examples, click here.|
|`issue list --my-open-issues` | Shortcut which displays all issues assigned to you, which are open.|
|`issue list --my-issues` | Shortcut which displays all issues assigned to you.|

|Detailed Issue View Commands|Description|
|---|---|
|`issue show <issue_id>` | Displays the selected issue in detail.|
|`issue show --with-comments <issue_id>` | Displays the selected issue in detail, along with its comments.|
|`issue show --no-comments <issue_id>` | Displays the selected issue's comments only.|

|Miscellaneous Commands|Description|
|---|---|
|`issue init` | Creates an empty config file in the current directory.|
|`issue version` | Displays the current version of the tool.|
|`issue help` | Displays a menu with usage instructions for each command.|

---------
### Listings Search Parameters

|Search Parameter|Possible Values|
|---|---|
|`--assignee_id`| (integer/Any/None)|
|`--assignee_username`| (comma-separated-strings)|
|`--created_after`| (datetime)|
|`--created_before`| (datetime)|
|`--updated_after`| (datetime)|
|`--updated_before`| (datetime)|
|`--labels`| (comma-separated-strings)|
|`--search`| (string)|
|`--order_by`| (created_at/updated_at/)|
|`--state`| (opened/closed)|


**Examples;**
```
issue list --my-open-issues --labels backend,doing --created_before --created_before 2012-12-21
issue list --assignee_username sauron123 --assignee_username frodo99
```

# Potential Contributions
Feel free to submit an MR for a feature addition.

# Tools Used
* Gitlab APIs
* Vim
