# gh-me

> 🔀 A compact, accessible GitHub CLI extension for listing your PRs, issues, and review requests.

## 🛠️ Features
✅ **Lists your open PRs by default**  
✅ **Supports draft PRs with `--draft`**  
✅ **Lists open issues with `gh-me issues`**  
✅ **Shows PRs where you're a reviewer with `gh-me reviews`**  
✅ **Filters PRs, issues, and reviews by organization with `--org=<organization>`**  
✅ **Color-coded for accessibility**  
✅ **Compact, easy-to-read formatting**  

---

## 🔨 Installation

Install the extension via GitHub CLI:

```sh
gh extension install jimmy-guzman/gh-me
```

Or, if developing locally:

```sh
gh extension install .
```

---

## 🔍 Usage

### **Listing Pull Requests (Default)**
Running `gh-me` **defaults to listing PRs**:

```sh
gh-me
```

```
PR#     REPOSITORY                     TITLE                                      REVIEW      URL
----    -----------------------------  -----------------------------------------  ----------  -----------------------------------------------
#77     jimmy-guzman/comparto-eslint   feat(*): ✨ everything is configurable...  PENDING     https://github.com/jimmy-guzman/comparto-eslint-config/pull/77
#1      jimmy-guzman/jimmyguzman.com   first release                             PENDING     https://github.com/jimmy-guzman/jimmyguzman.com/pull/1
```

### **Filtering PRs by Organization**
To only show PRs from a specific **GitHub organization**, use:

```sh
gh-me prs --org=jimmy-guzman
```

```
PR#     REPOSITORY                     TITLE                                      REVIEW      URL
----    -----------------------------  -----------------------------------------  ----------  -----------------------------------------------
#12     jimmy-guzman/ui                Fix button styles                          APPROVED    https://github.com/jimmy-guzman/ui/pull/12
```

### **Including Draft PRs**
Use the `--draft` flag to include **draft PRs**:

```sh
gh-me prs --draft
```

```
PR#     REPOSITORY                     TITLE                                      REVIEW      URL
----    -----------------------------  -----------------------------------------  ----------  -----------------------------------------------
#77     jimmy-guzman/comparto-eslint   feat(*): ✨ everything is configurable...  PENDING     https://github.com/jimmy-guzman/comparto-eslint-config/pull/77
#10     jimmy-guzman/experimental      WIP: Add experimental changes             DRAFT       https://github.com/jimmy-guzman/experimental/pull/10
```

---

### **Listing Issues**
To list **your open issues**, use:

```sh
gh-me issues
```

```
ISSUE#  REPOSITORY                     TITLE                                      URL
------  -----------------------------  -----------------------------------------  -----------------------------------------------
#252    jimmy-guzman/popcorn.fyi       Error in protected pages during load      https://github.com/jimmy-guzman/popcorn.fyi/issues/252
#251    jimmy-guzman/popcorn.fyi       Double quotes                             https://github.com/jimmy-guzman/popcorn.fyi/issues/251
```

### **Filtering Issues by Organization**
To only show issues from a specific **GitHub organization**, use:

```sh
gh-me issues --org=jimmy-guzman
```

```
ISSUE#  REPOSITORY                     TITLE                                      URL
------  -----------------------------  -----------------------------------------  -----------------------------------------------
#12     jimmy-guzman/api               Add new GraphQL resolver                   https://github.com/jimmy-guzman/api/issues/12
```

---

### **Listing PRs Where You're a Reviewer**
To see PRs where you've been **requested for review**, use:

```sh
gh-me reviews
```

```
PR#     REPOSITORY                     TITLE                                      URL
----    -----------------------------  -----------------------------------------  -----------------------------------------------
#32     jimmy-guzman/api               Add new GraphQL resolver                   https://github.com/jimmy-guzman/api/pull/32
#15     jimmy-guzman/ui                Improve button accessibility               https://github.com/jimmy-guzman/ui/pull/15
```

---

### **Filtering Reviews by Organization**
To **only show PRs where you've been requested as a reviewer** in a specific organization, use:

```sh
gh-me reviews --org=jimmy-guzman
```

```
PR#     REPOSITORY                     TITLE                                      URL
----    -----------------------------  -----------------------------------------  -----------------------------------------------
#45     jimmy-guzman/api               Improve GraphQL mutations                  https://github.com/jimmy-guzman/api/pull/45
#27     jimmy-guzman/frontend          Refactor navbar component                  https://github.com/jimmy-guzman/frontend/pull/27
```

---

## 🚀 Roadmap
- 🛠️ **Additional sorting flags for PR & Issues filtering**
- 🛠️ **Additional filter flags for PR & Issues filtering**
- 🛠️ **More GitHub activity commands (stars, notifications, etc.)**
