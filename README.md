# django-template-hexencoder

A template library providing tags/filters for common operations with strings from/to hex conversion

For now this little library is pretty simple, it provides only a few tags that I needed in my personal website. It may be expanded in the future.

# Usage

Add 'hexencoder' to your INSTALLED_APPS:

```python
INSTALLED_APPS = (
    'django.contrib.admin',
    'django.contrib.auth',
    # ... 
    'hexencoder',
)
```

Now use the hexencoder library inside your templates:

```html
{% load hexencoder %}

<p>My e-mail address is:</p>

<script type="text/javascript">
	document.write(
    	unescape(
        	"{% convert_hex_percent 'mail@example.com' %}"
        )
    );
</script>
```

Or use the shorthand version:


```html
{% load hexencoder %}

<p>My e-mail address is: {% convert_hex_js 'mail@example.com' %}</p>
```
