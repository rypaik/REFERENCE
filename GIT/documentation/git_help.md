usage: git [--version] [--help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           <command> [<args>]

These are common Git commands used in various situations:

start a working area (see also: git help tutorial)
   clone             Clone a repository into a new directory
   init              Create an empty Git repository or reinitialize an existing one

work on the current change (see also: git help everyday)
   add               Add file contents to the index
   mv                Move or rename a file, a directory, or a symlink
   restore           Restore working tree files
   rm                Remove files from the working tree and from the index
   sparse-checkout   Initialize and modify the sparse-checkout

examine the history and state (see also: git help revisions)
   bisect            Use binary search to find the commit that introduced a bug
   diff              Show changes between commits, commit and working tree, etc
   grep              Print lines matching a pattern
   log               Show commit logs
   show              Show various types of objects
   status            Show the working tree status

grow, mark and tweak your common history
   branch            List, create, or delete branches
   commit            Record changes to the repository
   merge             Join two or more development histories together
   rebase            Reapply commits on top of another base tip
   reset             Reset current HEAD to the specified state
   switch            Switch branches
   tag               Create, list, delete or verify a tag object signed with GPG

collaborate (see also: git help workflows)
   fetch             Download objects and refs from another repository
   pull              Fetch from and integrate with another repository or a local branch
   push              Update remote refs along with associated objects

'git help -a' and 'git help -g' list available subcommands and some
concept guides. See 'git help <command>' or 'git help <concept>'
to read about a specific subcommand or concept.
See 'git help git' for an overview of the system.

-------

## NAME

git-ls-files - Show information about files in the index and the working tree

## [](https://git-scm.com/docs/git-ls-files#_synopsis)SYNOPSIS

*git ls-files* [-z] [-t] [-v] [-f]
        (--[cached|deleted|others|ignored|stage|unmerged|killed|modified])*
        (-[c|d|o|i|s|u|k|m])*
        [--eol]
        [--deduplicate]
        [-x <pattern>|--exclude=<pattern>]
        [-X <file>|--exclude-from=<file>]
        [--exclude-per-directory=<file>]
        [--exclude-standard]
        [--error-unmatch] [--with-tree=<tree-ish>]
        [--full-name] [--recurse-submodules]
        [--abbrev[=<n>]] [--] [<file>…​]

## [](https://git-scm.com/docs/git-ls-files#_description)DESCRIPTION

This merges the file listing in the index with the actual working
directory list, and shows different combinations of the two.

One or more of the options below may be used to determine the files
shown:

## [](https://git-scm.com/docs/git-ls-files#_options)OPTIONS

[](https://git-scm.com/docs/git-ls-files#Documentation/git-ls-files.txt--c)-c

[](https://git-scm.com/docs/git-ls-files#Documentation/git-ls-files.txt---cached)--cached

Show cached files in the output (default)

[](https://git-scm.com/docs/git-ls-files#Documentation/git-ls-files.txt--d)-d

[](https://git-scm.com/docs/git-ls-files#Documentation/git-ls-files.txt---deleted)--deleted

Show deleted files in the output

[](https://git-scm.com/docs/git-ls-files#Documentation/git-ls-files.txt--m)-m

[](https://git-scm.com/docs/git-ls-files#Documentation/git-ls-files.txt---modified)--modified

Show modified files in the output

[](https://git-scm.com/docs/git-ls-files#Documentation/git-ls-files.txt--o)-o

[](https://git-scm.com/docs/git-ls-files#Documentation/git-ls-files.txt---others)--others

Show other (i.e. untracked) files in the output

[](https://git-scm.com/docs/git-ls-files#Documentation/git-ls-files.txt--i)-i

[](https://git-scm.com/docs/git-ls-files#Documentation/git-ls-files.txt---ignored)--ignored

Show only ignored files in the output. When showing files in the
index, print only those matched by an exclude pattern. When
showing "other" files, show only those matched by an exclude
pattern. Standard ignore rules are not automatically activated,
therefore at least one of the `--exclude*` options is required.

[](https://git-scm.com/docs/git-ls-files#Documentation/git-ls-files.txt--s)-s

[](https://git-scm.com/docs/git-ls-files#Documentation/git-ls-files.txt---stage)--stage

Show staged contents' mode bits, object name and stage number in the output.

[](https://git-scm.com/docs/git-ls-files#Documentation/git-ls-files.txt---directory)--directory

If a whole directory is classified as "other", show just its
name (with a trailing slash) and not its whole contents.

[](https://git-scm.com/docs/git-ls-files#Documentation/git-ls-files.txt---no-empty-directory)--no-empty-directory

Do not list empty directories. Has no effect without --directory.

[](https://git-scm.com/docs/git-ls-files#Documentation/git-ls-files.txt--u)-u

[](https://git-scm.com/docs/git-ls-files#Documentation/git-ls-files.txt---unmerged)--unmerged

                                        ░▒▓ 08:59:46 

▶ ls
