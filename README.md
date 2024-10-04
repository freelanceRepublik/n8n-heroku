# frk-n8n

Configuration n8n pour les services frk-n8n-staging et frk-n8n-production

## Installation initiale

```
heroku git:remote -a frk-n8n-staging -r frk-n8n-staging
heroku git:remote -a frk-n8n-production -r frk-n8n-production
git push --set-upstream frk-n8n-staging main
git push --set-upstream frk-n8n-production main
```

## Update

Principe : forcer un rebuild du Dockerfile

```
git commit --allow-empty -m "Update to latest version"
git push frk-n8n-staging main
```

Ref : https://help.heroku.com/18PI5RSY/how-do-i-clear-the-build-cache

![Capture d’écran 2024-10-04 à 11 14 51](https://github.com/user-attachments/assets/142ed52d-5df8-4848-a334-8e3073210bf4)
