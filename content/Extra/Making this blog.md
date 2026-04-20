# Quartz
Quartz is a static site generator that uses markdown files and turns them into html web pages, this tool is amazing as it I have created my devlog using obsidian notes it allows me to create notes and documents easily as I find that markdown is the best language to create documents like this with.
## Obsidian notes
First I started with Obsidian notes which is an open source markdown editor, Obsidian has many features like the graph view which makes it easy to navigate large and complex notes. However I do not have to use Obsidian there are several alternatives including visual studio code or vim/neovim, both of these are more oriented to programming and do not display the markdown preview like Obsidian dose 
![[Pasted image 20260413124722.png]]

## Quartz
To set up quartz I went to the documentation of the software and found a setup command
(A little side note! because I had my own computer while on campus I decided to do make this on Linux however everything development was done on windows sadly)
```zsh
git clone https://github.com/jackyzha0/quartz.git
cd quartz
npm i
npx quartz create
```
After running this command the terminal shows a setup menu allowing me to pick a few options which sets up the software initially.

now to create a preview of my website i rand the command `npx quartz build --serve` in my terminal, this creates a preview of my website hosted on my computer which I can view from my web browser.
![[Pasted image 20260413131559.png]]
After making sure my website works I then synced the repository to GitHub using, however I ran into an issue with connecting to my github account due to being on linux git wants an ssh key instead of a login so I had to create one in my account settings and change a few config files.
![[Pasted image 20260413132136.png]]
For the final step to deploy my blog onto the internet I had to add a GitHub workflow that actually deploys the website first I opened the quartz folder in Neovim and then created a new file in the workflows folder called `deploy.yml`, the quartz documentation gives a template which I copied most of it with the exception being that I changed the branch from V4 to main.
![[Pasted image 20260413140028.png]]
After this I ran `npx quartz sync` which syncs the files to GitHub as well as run the deploy action posting it on the internet.
### Neovim
As an extra note Neovim is a very complex text editor that I use. by default it opens as a blank page similar to windows notepad, compared to windows notepad or visual studio code it has a lot of differences the main one being that in runs in the terminal and that it dose not use conventional keybindings like a normal text editor, for example instead of pressing `CTRL + S` to save a document you press `SHIFT + :` to open the command palliate where you can type commands which correspond to actions for this case you type `w` and enter to save the file. Compared to traditional text/code editors I find Neovim to be significantly better than traditional text editors.
Alongside default Neovim I also installed LazyVim which is an add-on for Neovim that adds several features including the file tree on the side.