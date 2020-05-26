# Templates in App Folders

The point of this repo is to show how Django handles templates when you have a separate `templates` directory for each app. Each directory is located at the top level of the app; Django will discover them automatically.

### Pros

- Easy to find app-specific templates

### Cons

- Django will always grab the first template that it finds with the right name. If you have three apps that all use `index.html`, `return render(request, "index.html")` will always return the first `index.html` it finds in _any template folder_. This requires that each template have a different name.

This is part of a set of repos.

- https://github.com/itsthejoker/templatedemo-sharedfolder
- https://github.com/itsthejoker/templatedemo-individualfolders <-- you are here
