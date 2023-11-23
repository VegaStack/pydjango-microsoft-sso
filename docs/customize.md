# Customizing the Login Page
Below, you can find some tips on how to customize the login page.

## Hiding the Login Form

If you want to show only the Microsoft Login button, you can hide the login form using
the `SSO_SHOW_FORM_ON_ADMIN_PAGE` setting.

```python
# settings.py

SSO_SHOW_FORM_ON_ADMIN_PAGE = False
```

## Customizing the Login button

Customizing the Login button is very simple. For the logo and text change is straightforward, just inform the new
values. For
the style, you can override the css file.

### The button logo

To change the logo, use the `MICROSOFT_SSO_BUTTON_LOGO` setting.

```python
# settings.py
MICROSOFT_SSO_LOGO_URL = "https://example.com/logo.png"
```

### The button text

To change the text, use the `MICROSOFT_SSO_BUTTON_TEXT` setting.

```python
# settings.py

MICROSOFT_SSO_TEXT = "New login message"
```

### The button style

The login button css style is located at
`static/django_microsoft_sso/microsoft_button.css`. You can override this file as per Django
[static files documentation](https://docs.djangoproject.com/en/4.2/howto/static-files/).

#### An example

```python
# settings.py

MICROSOFT_SSO_TEXT = "Login using Microsoft 365 Account"
```

```css
/* static/django_microsoft_sso/microsoft_button_custom.css */

/* other css... */

.microsoft-login-btn {
    background-color: darkcyan;
    border: 1px solid #a7a7a7;
    padding: 1px;
    margin-bottom: 10px;
    width: 100%;
}
```

The result:

![](images/django_login_with_microsoft_custom.png)
