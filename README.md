# ud303_Bookmark_Server
A simple URL shortener server,  project from Udacity course (ud303).

## Demo

- [Bookmark Server](https://ud303-bookmark-server-loukei.herokuapp.com/)

## Bug tracks

### Q: fatal: 'heroku' does not appear to be a git repository

#### ANS

`heroku git:remote -a ud303-bookmark-server-loukei`

#### Reference

- [實作：部署 Rails 專案上 Heroku 遇到的 8 個困難與解決方式 | by 涓 / Lynn Chang | Lynn’s dev blog | Medium](https://medium.com/lynns-dev-blog/%E5%AF%A6%E4%BD%9C-%E9%83%A8%E7%BD%B2-rails-%E5%B0%88%E6%A1%88%E4%B8%8A-heroku-%E9%81%87%E5%88%B0%E7%9A%84-8-%E5%80%8B%E5%9B%B0%E9%9B%A3%E8%88%87%E8%A7%A3%E6%B1%BA%E6%96%B9%E5%BC%8F-381f6cb6330e)

### Q: No default language could be detected for this app.

#### ANS: 

Make sure all `requirements.tx`, `Procfile`, `runtime.tx` in root folder.
Check `Procfile` after you change `main.py` location.
Then push to heroku again.

#### Refernece

- [heroku/heroku-buildpack-python - Buildpacks - Heroku Elements](https://elements.heroku.com/buildpacks/heroku/heroku-buildpack-python)

> A requirements.txt must be present at the root of your application's repository to deploy.
> To specify your python version, you also need a runtime.txt file - unless you are using the default Python runtime version.
> Current default Python Runtime: Python 3.10.4
> Alternatively, you can provide a setup.py file, or a Pipfile. Using pipenv will generate runtime.txt at build time if one of the field python_version or python_full_version is specified in the requires section of your Pipfile.

### Q:How to set environment root path when server code deployee to cloud?

#### Ans

Don't use any hardcode URI in any place(frontend and backend). Use `/` instaed.

### Q:Use github deployee to heroku

[GitHub Integration (Heroku GitHub Deploys) | Heroku Dev Center](https://devcenter.heroku.com/articles/github-integration)