---
layout: entry
title:  "Main content"
categories: main

keyboard:
  skip-links: |
    Focus moves directly to the main content area
  tab: |
    Links and buttons within the main area are focusable
    
name:  |
  Discoverable by screen reader as main landmark
role:  |
  Identifies itself as a main landmark
group: |
  Typically contains the content of the page
state: |
  n/a
      
mobile:
  swipe: |
    Focus moves within main area

---

## Code examples

### Use semantic HTML
This semantic HTML contains all accessibility features by default.

{% highlight html %}
<main tabindex="-1" id="content"> 
  <h1>About our company</h1>
  <p>The main content of the page belongs here.</p>
</main>
{% endhighlight %}

### Avoid custom elements
This custom main element requires extra attributes.

{% highlight html %}
<div role="main" tabindex="-1" id="content"> 
  <h1>About our company</h1>
  <p>The main content of the page belongs here.</p>
</div>
{% endhighlight %}

## Developer notes

### Name
- Typically doesn't have a name other than its role.

### Role

- Identifies itself as a main landmark
- If a non-semantic element must be used (like a `<div>`) use `role="main"`.

### Group

- Should contain the main content of the page.

### Focus

- Can be targeted with a skip link, but isn't focusable with the tab key
- Use `tabindex="-1"` to make the main targetable with a skip link.

