---
theme: ./
---

# Slidev Theme Starter

Presentation slides for developers

<div class="pt-12">
  <span @click="next" class="px-2 p-1 rounded cursor-pointer hover:bg-white hover:bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

---

# What is Slidev?

Slidev is a slide maker and presentation tool designed for developers. It includes the following features:

- 📝 **Text-based** - focus on your content with Markdown, then style it later
- 🎨 **Themable** - themes can be shared and reused as npm packages
- 🧑‍💻 **Developer Friendly** - code highlighting, live coding with autocompletion
- 🤹 **Interactive** - embed Vue components to enhance your expressions
- 🎥 **Recording** - built-in recording and camera view
- 📤 **Portable** - export to PDF, PPTX, PNGs, or even a hostable SPA
- 🛠 **Hackable** - virtually anything that's possible on a webpage is possible in Slidev

<br>
<br>

Read more about [Why Slidev?](https://sli.dev/guide/why)

---

# Navigation

Hover on the bottom-left corner to see the navigation's controls panel

## Keyboard Shortcuts

|     |     |
| --- | --- |
| <kbd>space</kbd> / <kbd>tab</kbd> / <kbd>right</kbd> | next animation or slide |
| <kbd>left</kbd>  / <kbd>shift</kbd><kbd>space</kbd> | previous animation or slide |
| <kbd>up</kbd> | previous slide |
| <kbd>down</kbd> | next slide |

---
layout: image-right
image: https://cover.sli.dev
---

# Code

Use code snippets and get the highlighting directly!

```ts
interface User {
  id: number
  firstName: string
  lastName: string
  role: string
}

function updateUser(id: number, update: Partial<User>) {
  const user = getUser(id)
  const newUser = { ...user, ...update }
  saveUser(id, newUser)
}
```

---
layout: center
class: "text-center"
---

# Learn More

[Documentation](https://sli.dev) / [GitHub Repo](https://github.com/slidevjs/slidev)


---
layout: header-with-one-column
---

## Text Styling

::body::
* **Bold**
* *italics*
* <u>underline</u>
* <a href="#">link</a>

---
layout: header-with-two-columns
---

# Additional Stuff

::left::
* a
* b
* c

::right::
1. one
2. two
3. three

---
layout: two-headers-with-two-columns
---

::left-header::
## Example 1

::left::

* a
* b
* c

::right-header::
## Example 2

::right::

1. one
2. two
3. three

---
layout: two-headers-with-two-header-columns
---

# Main Header

::left-header::
## Left Subheader

::left::
* a
* b
* c

::right-header::
## Right Subheader

::right::
1. one
2. two
3. three

---
layout: quote-with-image
image: https://cs.unc.edu/wp-content/uploads/sites/1265/2013/12/fred-brooks-300x300.jpg
author: Fred P. Brooks
---
"Adding manpower to a late software project makes it later."


