django-simple-deploy
===

> Deployment, for Djangonauts with deadlines.

`django-simple-deploy` provides a management command that configures your project for an initial deployment. The plugin-based architecture means it can support deployment to just about any host that can be configured to serve a Django project.

Here's the simplest way to deploy a project to Fly.io:

```sh
$ pip install "django-simple-deploy[fly_io]"
# Add django_simple_deploy to INSTALLED_APPS
$ python manage.py deploy --automate-all
```

This will configure your project for deployment to Fly.io, commit the configuration changes, and push your code to Fly's servers. If you want more control, there's a configuration-only mode that lets you inspect your project before committing changes, and lets you run the command that pushes your code.

You can deploy to any host that has an active django-simple-deploy plugin. Currently that's Fly.io, Platform.sh, and Heroku. The `dsd-vps` plugin is currently under development; it will support deployment to any VPS-based hosting provider.

For more information, see the core [django-simple-deploy](https://github.com/django-simple-deploy/django-simple-deploy) project, or any of the existing plugins.
