# Bootstrapping Bulletin Board 1

<div class="bg-blue-100 py-1 px-5" markdown="1">

Before you begin here, make sure you have gone through the [Bootstrap Levels lesson](https://learn.firstdraft.com/lessons/139-intro-to-bootstrap).
</div>

In this project, we'll practice using bootstrap.css to make our apps look professional.

[Here is our target.](https://bulletin-board-bootstrap.matchthetarget.com/)

You can peek at the source code of the target when you get stuck.

## Setup

There are no automated tests in this project, so you should [fork the bulletin-board-1-twbs repository directly](https://github.com/appdev-projects/bulletin-board-1-twbs/fork) and set up a codespace as usual.

Then:

- `bin/dev`
- `rake sample_data`
- Look around the live app preview and the codebase. You'll see that our starting point is the solution to the Bulletin Board 1 project.
- Make Git commits and Format Document often as you work.

<aside markdown="1">

When copy-pasting code into HTML documents, you can auto-format the indentation so that the elements are properly nested using <kbd>Cmd</kbd> + <kbd>shift</kbd> + <kbd>p</kbd> (Mac) or <kbd>Cntrl</kbd> + <kbd>shift</kbd> + <kbd>p</kbd> (Windows) to open the **command pallet** in VSCode. 

With the `>` command pallet prompt open, you can search "Format" and find the command. (You can search for any command in this prompt.) You will also see a direct keyboard shortcut to that formatting command that might be useful to you. Become a keyboard ninja!
</aside> 

## Hints


### Application layout

In the application layout file:

- Add bootstrap.css and all of its plugins by putting this in the `<head>`:

```html
<!-- Connect Bootstrap CSS -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/css/bootstrap.min.css">

<!-- Connect Bootstrap JavaScript and its dependencies -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/js/bootstrap.bundle.min.js"></script>
```

- Add Font Awesome by putting this in the `<head>`:
		
```html
<!-- Connect Font Awesome -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.1/js/all.min.js"></script>
```

- Make the pages responsive by putting this in the `<head>`:

```html
<meta name="viewport" content="width=device-width, initial-scale=1">
```

- Make the `notice` and `alert` flash messages more attractive with the Bootstrap [Alert component](https://getbootstrap.com/docs/5.3/components/alerts/).
- [Add a Navbar.](https://getbootstrap.com/docs/5.3/components/navbar/#nav)

### boards#index

- Use [the Card component with a flush List Group](https://getbootstrap.com/docs/5.3/components/card/#list-groups) for the boards#index page.
- In order to place the "Add a new board" button on the right side of the card-header, use [the `d-flex` utility](https://getbootstrap.com/docs/5.3/utilities/flex/).

    Then add `ms-auto` to the element you want to be pushed to the right side.
- Use Font Awesome for [the right-pointing arrow (chevron-right)](https://fontawesome.com/icons/chevron-right?f=classic&s=solid).
- To constrain and center the card, use [the Grid](https://getbootstrap.com/docs/5.3/layout/grid/). Create a row with a single, 6-column cell. Offset it by 3 cells. Put the card within it.
- To hide the new board form until the user asks for it, use [a Modal](https://getbootstrap.com/docs/5.3/components/modal/#live-demo).

### boards#show

- Use [Tabs](https://getbootstrap.com/docs/5.3/components/navs-tabs/#javascript-behavior) to separate active and expired posts. You can make the tabs occupy the whole width of the screen with [.nav-fill](https://getbootstrap.com/docs/5.3/components/navs-tabs/#fill-and-justify).
- Use [Grid cards](https://getbootstrap.com/docs/5.3/components/card/#grid-cards) to lay out active posts.
		
## Solution

You can [View Source on the target](https://bulletin-board-bootstrap.matchthetarget.com/) to see how I did things.
