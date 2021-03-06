# Reusable Layout Components for CN Platform

- Objective
- Where?
- Components
    * Tags (Dividers)
        - Section Dividers
        - Assignment Dividers
    * Headings
    * Resources
    * Tasks
    * Quotes
    * Code Blocks
- Formatting
    * Code Blocks
    * Code font size
    * Documentation font size


## Objective

Lay the groundwork for **unified and adaptable styling** across all courses on the whole site.

- **simple**: simple elements favored over complex ones (easier to set up and maintain)
- **reusable components**: HTML elements with CSS classes
- **centralized**: Styling only through SCSS in Maker Theme
- **maintainable**: Edit centrally, avoid unnecessary effort and potential misalignment

## Where?

`Site administration / Appearance / Maker / Advanced Settings / Raw SCSS`

**Design changes** for these components can be made centrally in the [**Maker** Theme settings](https://platform.codingnomads.co/learn/admin/settings.php?section=themesettingmaker). Click into the "Advanced Settings" tab and add/change CSS inside the second SCSS box.

---

## Components

Components to use when creating and editing courses. Add new components in this section.

### Weekly Breakdowns

To help students stay on track, add weekly breakdowns in the "Summary" of each section (Edit Topic)

```html
<h3 class="week week-1">Week 1 - Part 1</h3>
```

Different weeks can be given different styles, so add also the `week-#` class appropriately, e.g.:

```html
<h3 class="week week-3">Week 3 - Part 3</h3>
```

### Tags (Dividers)

#### Section Dividers

```html
<h5 class="section-divider">Section Mini-Heading</h5>
```

#### Assignment Dividers

```html
<h5 class="section-assignment">Assignments</h5>
```

![dividers](imgs/dividers.png)

### Headings

**Use Editor-provided headings**:

- "Heading (large)" option creates `<h3>` element
- "Heading (medium)" option creates `<h4>` element
- "Heading (small)" option creates `<h5>` element

**Don't apply editor styles to headings** - we can increase heading size, font-weight,
etc. centrally through SCSS.

### Information

Use this bootstrap alert box to include information about upcoming course sections. E.g.: "Just read over this for now, we'll dig deepr into it in a later section."

```html
<div class="alert alert-warning" role="alert">
  Infos about upcoming course sections.
</div>
```

### Resources

```html
<div class="jumbotron resources">
<h1>Resources</h1>
</div>
```

Paste HTML into HTML editor of Page Activity.
Switch to Editor view and copy-paste your Resource links into the body of the jumbotron, and style as bullet point list.


resources](resources.png)

### Tasks

```html
<div class="jumbotron tasks">
<h1>Tasks</h1>
</div>
```

Same as for Resources.

![resources](imgs/tasks.png)

### Quotes

Minimal example:

```html
<div class="quote-card">
    <p>Quote goes here</p>
    <cite><a href="RESOURCE_URL">resource name</a></cite>
</div>
```

![quote](imgs/quote.png)

Check out the [Maker Theme SCSS](https://platform.codingnomads.co/learn/admin/settings.php?section=themesettingmaker) for more options.


### Code Blocks

Wrap code snippets into triple-backticks:

    ```
    print("your code here")
    ```

Note: Syntax highlighting is sometimes broken.


### In-line Code

Currently no straightforward button to do this. Therefore, switch to the _HTML editor_ and wrap in-line code snippets into `<code>your_code()</code>` tags.

---

## Formatting

Collection of style changes and justification for those changes.

### Code font size

Slightly increased code font-size: `code {font-size: 1.1em;}`. It was hard to read the code before.


### Documentation font size

General font-size is currently also relatively small, could be increased.
