# My Website
* Using [H.U.G.O](https://gohugo.io/) framework
* Theme: [PaperMod](https://themes.gohugo.io/themes/hugo-papermod/)
  This was added using subtree to fix the version and allow easy changes
  ```bash
  git subtree add --squash -P themes/PaperMod https://github.com/adityatelange/hugo-PaperMod.git master
  ```



## Custom configuration

* `overview: true` on a page: display it on the home page



## Issues encountered

#### Posts not showing on the first page
* The page can not be in "profile mode"
* The files must be in the folder `content/posts/`
* There can not be any folder with file in `content/` that is alphabetically before `content/posts/`