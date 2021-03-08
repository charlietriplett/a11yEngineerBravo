---
layout: entry
title:  "Link"
categories: navigation
order: 1

keyboard:
  tab: |
    Focus visibly moves to the link.
  enter: |
    Activates the link.

name:  |
  Purpose is clear
role:  |
  Identifies itself as a link
group: |
  n/a
state: |
  n/a
            
mobile:
  swipe: |
    Focus moves to the element
  doubletap: |
    Activates the link
---

## Code examples

### Use semantic HTML
This semantic HTML contains all accessibility features by default. 

{% highlight html %}
<a href="/about/">
  About
</a>
{% endhighlight %}

{% raw %}
<a href="/about/">
  About
</a>
{% endraw %}

If a link has no definable url, add `tabindex="0"` to make it focusable.

{% highlight html %}
<a tabindex="0">
  About
</a>
{% endhighlight %}

{% raw %}
<a tabindex="0">
  About
</a>
{% endraw %}

### Avoid custom elements
This custom button requires extra attributes and event listeners.

{% highlight html %}
<custom-element role="link" tabindex="0">
  About
</custom-element>
{% endhighlight %}

## Developer notes

### Name
- Inner text should describe the purpose of the link.
- **Do not** repeat the name with `aria-label="Link purpose"` 

### Role
- Native button identifies as button by default
- Use `role="link"` for custom elements

### Focus
- Focus must be visible
- Custom elements need `tabindex="0"` to be focusable
