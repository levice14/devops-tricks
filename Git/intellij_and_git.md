Git commands you can combine with IntelliJ features -- examples via [CloudSlang](https://github.com/CloudSlang)

-	list remotes: `git remote [-v]`

![list_remotes](http://imgur.com/SOxjjAw.png)

![list_remotes_verbose](http://imgur.com/u9jAoI5.png)

- add remote: `git remote add <remote_name> git@github.com:<gh_user>/cloud-slang.git`

![add_remote](http://i.imgur.com/9CZSWnp.png)

- get the stuff: `git fetch <remote_name>`

![fetch](http://imgur.com/dQnu1kJ.png)

-	now you can access remotes / branches from IntelliJ UI:

![intellij_ui](http://imgur.com/xKLtf05.png)

- once you have too many remotes / branches you can clean up with:

  - delete all branches other than master: `git branch | grep -v " master$" | xargs git branch –D`
  - delete all remotes other than origin/genadi: `git remote | grep -v "^origin\|genadi$" | xargs -I {} git remote remove {}`
    - of course these commands can slightly differ depending on your env – for a more robust solution, you should write a CloudSlang flow :)
