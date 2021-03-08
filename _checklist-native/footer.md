---
layout: entry
title:  "Footer / contentinfo"
categories: footer

keyboard:
  skip-links: |
    Focus moves directly to the footer
  tab: |
    Links and buttons within the footer are focusable
    
name:  |
  Discoverable by screen reader as footer or contentinfo landmark
role:  |
  Identifies itself as a footer or contentinfo landmark
group: |
  Typically contains copyright information, navigation links, and privacy statements.
state: |
  n/a
      
mobile:
  swipe: |
    Focus moves within footer.
  doubletap: |
    This typically activates most elements.

---

## Code examples

### Use semantic HTML
This semantic HTML contains all accessibility features by default.

{% highlight html %}
{% include /examples/footer.html %}
{% endhighlight %}

{::nomarkdown}
{% include /examples/footer.html %}
{:/}

### Avoid custom elements
This custom footer requires extra attributes.

{% highlight html %}
<div role="contentinfo" tabindex="-1" id="footer">
  © 2021 Site Name
</div>
{% endhighlight %}

## Developer notes

### Name
- Typically doesn't have a name

### Role

- Identifies itself as a footer or contentinfo landmark
- If a non-semantic element must be used (like a `<div>`) use `role="contentinfo"`.

### Group

- Typically contains copyright information, navigation links, and privacy statements.

### Focus

- Can be targeted with a skip link, but isn't focusable with the tab key
- Use `tabindex="-1"` to make the footer targetable with a skip link.

