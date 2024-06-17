# Welcome to my website

## Workflow 

First, edit in `developerFolio (website-backend)`repository
```
npm run start
```
After check everything is ok, generate `biuld` folder in the `developerFolio (website-backend)` folder using
`npm run build`

After that, come to `my-wesite` folder now.

`git checkout dev`

Then reset 'gh-pages' branch by
```
git branch -D gh-pages
git checkout -b gh-pages    
```

Next, copy files in `build` folder which generated before in the `website-backend` 
and paste into `gh-pages`.

Finally, push `gh-pages` to remote `origin/gh-pages`

`git push --set-upstream origin gh-pages`

The details can be find at [here](https://chengmatengblog.netlify.app/post/2fbd.html)
