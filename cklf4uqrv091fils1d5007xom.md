## NVM NOT FOUND?

## NVM Not Found after Pimping Terminal with oh-my-zsh?

Have you finished configuring your terminal?  
Looking so cool now, but while can't I make use of my favorite tools after the Pimp?

![Screenshot_2021-02-21_12-27-41.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1613907119527/Bz4J7BwD1.png)

I have encountered this issue every time I pimp my terminal, so today I have decided to share with everyone how I did it.

**Why does this happen**

This happens because when installing NVM it adds code to `~/.bashrc`, as your default terminal now uses `zsh` and not bash it never reads ~/.bashrc and therefore never loads NVM.

To avoid this at installation, you can simply put `zsh` at the end of the curl command. 

Example:

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.37.2/install.sh | zsh
```

"In other words: this is NVMs fault, not yours."


**Solution:**

To fix this, all we need to do is tell the `~/.zshrc` to load `nvm` on the prompt.

From your terminal, open the `.zshrc` file with your favorite editor, `nano` will be just fine.

`nano .zshrc`

And paste the following line of command at the top:

```bash
. "$HOME/.nvm/nvm.sh"
```

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1613911386360/z1n5BnhfS.png)

Save the file `ctrl + s` and `ctrl + x` to exit

Restart your terminal, everything should work just fine now.

![".gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1613908634481/gY9CYLT1H.gif)

See you soon!