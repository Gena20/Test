Git

-   Basics
    -   Types of files
        -   Untracked (git doesn't know about these files)
        -   Tracked
            -   Unmodified
            -   Modified
            -   Staged (ready to commit)
    -   Types of objects
        -   Blob (representing the contents of file)
        -   Tree
        -   Commit
            -   A branch in Git is simply a lightweight movable pointer
                to one of these commits.
    -   Glob patterns
        -   Used in
            -   .gitignore
            -   git add "pattern"
            -   git rm "pattern" etc.
        -   Rules
            -   Blank lines or lines starting with \# are ignored.
            -   Standard glob patterns work, and will be applied
                recursively throughout the entire working tree.
            -   You can start patterns with a forward slash (/) to avoid
                recursivity.
            -   You can end patterns with a forward slash (/) to specify
                a directory.
            -   You can negate a pattern by starting it with an
                exclamation point (!).
        -   Syntax
            -   An asterisk (\*) matches zero or more characters
            -   [abc] matches any character inside the brackets (in this
                case a, b, or c)
            -   A question mark (?) matches a single character
            -   Brackets enclosing characters separated by a hyphen
                ([0-9]) matches any character between them (in this case
                0 through 9)
            -   You can also use two asterisks to match nested
                directories; a/\*\*/z would match a/z, a/b/z, a/b/c/z,
                and so on.
    -   Aliases
        -   Make an alias
            -   git config --global alias.comand
        -   Useful aliases
            -   alias.co=checkout
            -   alias.ci=commit
            -   alias.cim=commit -m
            -   alias.st=status
            -   alias.br=branch
            -   alias.hist=log --pretty=format:'%h %ad | %s%d [%an]'
                --graph --date=short
            -   alias.type=cat-file -t
            -   alias.dump=cat-file -p
            -   alias.a=add
-   Useful smth
    -   Base working with local
        -   git add
            -   To turn files from untracked into tracked
            -   To turn files from modified into staged
        -   git rm --cached To turn file form tracked into untracked
        -   git checkout -- To turn files from modified into unmodified
            like in the last commit
        -   git reset HEAD To turn files from staged into
            unstaged(modified)
        -   git commit | To commit all staged files