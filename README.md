django-seznam-captcha
=====================

Django captcha field and form using Captcha by [Seznam.cz](http://seznam.cz).

More information about Seznam captcha in docs <http://captcha-api.seznam.cz>

### Authors
*  Ondrej Sika, <http://ondrejsika.com>, ondrej@ondrejsika.com

### Source
* Python Package Index: <http://pypi.python.org/pypi/django-seznam-captcha>
* GitHub: <https://github.com/sikaondrej/django-seznam-captcha>

## Installation

install via pip

    pip install django-seznam-captcha
    
add to `INSTALLED_APPS` in `settings.py`

    INSTALLED_APPS += ("django_seznam_captcha", )

and add to root urls

    urlpatterns += url(r'^seznam-captcha/', include('django_seznam_captcha.urls'))


## Usage

use `django_seznam_captcha.fields.CaptchaField`

    from django import forms
    from django_seznam_captcha.fields import CaptchaField

    class MyForm(forms.Form):
        usename = forms.CharField()
        captcha = CaptchaField()

or create form from `django_seznam_captcha.forms.CaptchaForm`

    from django_seznam_captcha.forms import CaptchaForm
    
    class MyForm(CaptchaForm):
        username = forms.CharField()

        class Meta:
             fields = ("username", "captcha", )


[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/ondrejsika/django-seznam-captcha/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

