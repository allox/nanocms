install:

install ckEditor
https://github.com/django-ckeditor/django-ckeditor#installation

add to settings:

CKEDITOR_JQUERY_URL = "//ajax.googleapis.com/ajax/libs/jquery/2.1.1/jquery.min.js"
CKEDITOR_UPLOAD_PATH = "uploads/"
CKEDITOR_CONFIGS = {
    'awesome_ckeditor': {
        'toolbar': 'Full',
    },
    'default': {
        'toolbar': 'Basic',
        'height': 300,
        'width': 900,
    },
}


install nanocms:

 git clone https://github.com/allox/nanocms.git

add to urls:

    url(r'^page/',include('nanocms.urls')),

add to installed apps:
  'nanocms'

add to TEMPLATES:
  os.path.join(PROJECT_ROOT, 'nanocms/nanotemplates'),


(if not already) add django.contrib.humanize to installed_apps

 run migrations and collectstatic


Now it should be possible to access the CMS using  yourdomain.com/pages/admin

New page templates should be placed in the template-folder. (or linked to using ln -s )

