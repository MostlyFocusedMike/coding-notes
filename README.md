# My Coding Notes

## Format

They are all simple .txt files, so any program can read them, but they are meant to be read with in the command line or an IDE. All lines are formatted to be no more than 62 characters wide, so you can either have one open next to your IDE as you work, or an entire window devoted to several of them opened at once. 

(62 characters was chosen since it takes up 1/3 of a 15" screen using the [Spectacle](https://www.spectacleapp.com/) program, or half of a little 5" Raspberry Pi screen. Feel free to format them however you like!)  

## Navigation 
Any file inside the 0-polished-notes folder is nicely edited so that there is a table of contents. The strange #SSSS pattern is so you can easily jump from the table to the section using your program's search function. Each section starts with a clearly marked heading, and sub headings are strings of //////////// within the section.

Files are outside this folder if they lack that particular structure, they are also likely a lot less full. 

0-polished-notes is the folder name so it will come first when you bring it up the notes folder in the command line. You can either read and use the polished notes directly inside it, or use the symlinked files in the main folder. Symlinked files are missing the .txt extension so you can easily see what notes are polished.

## Grain of Salt 
These are my personal notes and I'm not a professional. So if an explanation is clunky, that's because I probably don't understand it  very well yet. I do try to go through and edit things as I learn, but these notes are intended for beginners like myself as a reference guide.

## VIM Files and Tips
The vimtutor abriged file is just the actual vimtutor's text with all the exercises removed. It's a good refresher after you've completed vimtutor. The cheat sheet is most of the basic commands taken from a github page by [awidegreen](https://gist.github.com/awidegreen/3854277#file-vim_cheatsheet-md).

To navigate all the notes easily in VIM, place your cursor onto a table of contents match pattern, then hit the * key in normal mode, this will jump you to the section.

To return to the table of contents just hit use the "gg" command in normal mode.

### ASCII art
All art was created using [patorjk.com's program.](http://patorjk.com/software/taag/#p=display&f=Big&t=Notes)
