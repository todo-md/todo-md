# TODO.md

Standard for markdown todo files.

## Specification

This document describes a multi project task management using standardized `TODO.md` markdown files.

Markdown todo files are simple markdown flavored text files. The TODO.md standard depicts an interchangeable standard for task management that is easily processable by machines and humans. It is aimed for teams and individuals that manage multiple project repositories and want to manage their todos the "git-way".

### Structure

The markdown todo files reside inside the project repository.

Here is an illustration:

```txt
.
├── project-a
│   ├── README.md
│   └── TODO.md
├── project-b
│   └── TODO.md
└── project-c
    └── TODO.md
```

Every todo markdown file starts with the `# TODO` header.

```markdown
# TODO

This text is not a task.

## Section

And this text neither.

- [ ] This task is open @owner

# BACKLOG

- [ ] This task is postponed

# DONE

- [x] This task is done #prio1
- [-] This task has been declined
```

Each subheader is a todo section. They help grouping and sorting the tasks.

The tasks themself are one liners that start with either `'- [ ] '`, `'- [-] '` or `'- [x] '`.

A task can be in the following states:

* open
* declined
* done
* deleted (removed from the document)

## Metadata

Tasks can be assigned to people using `@USERNAME` format.

Tasks can be tagged using the `#TAG` format.

## Hierarchy

When managing multiple markdown todo files the following hierarchy applies to all tasks.

1. Project: Name of the folder where the `TODO.md` reside.
2. Section: Subheader of `TODO.md` markdown content.
3. Task: File lines starting with `'- [ |-|x] '`

This hierarchy helps organizing and listing tasks either manually or using a software tool

# Example

Example for a todo file.

**TODO.md**

```markdown
# TODO

This is the markdown todo file for project a.

## Content

Tasks related to new content.

- [ ] Add readme file with newline #example

## Release

- [x] Init project repository
      http://github.com/todo-md/todo-md
- [ ] Publish project on GitHub @janikvonrotz

# DONE

- [x] Create GitHub organization tood-md
```

# Clients

* [todo-md-cli](https://github.com/todo-md/todo-md-cli) - Official TODO.md command line tool.

[Add your](https://github.com/todo-md/todo-md/issues/new) client or implementation of TODO.md to this readme file.
