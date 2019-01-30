# Codeanywhere Features
## Color Picker

The Color Picker makes it easy to create, adjust, and experiment with custom colors for your web site or application. Also it makes it easy to convert between HEX, RGB and RGBa color formats.

Color Picker is available in any file. You can open the Color Picker by hitting on Ctrl+Alt+K (PC) or CMD+Alt+K(MAC). It will appear as a pop-up near or below a text input field, allowing the user to select a color value, either decimal or hexadecimal (or both), by choosing the color with a mouse click, also the left slider selects the color code and right slider selects opacity value.

To close the Color Picker hit Enter, Esc or click outside Color Picker window.

![](/images/colorpicker.png)

## Share

Share with Codeanywhere is an amazing feature that lets you do more than just share your projects with any other Codeanywhere developer. You can grant someone else access to change files on your server, in real-time - or just let them view the files without any other rights.

To share your files on Codeanywhere, simply right click on Project, Connection, Folder or File you'd like to share and select Share. You'll be prompted to enter e-mails of the users you'd like to collaborate with.

![](/images/sharedialog.png)

In the Email field you can enter the email of the user that you want to share your file to. You can also set permissions for that share. Permissions are located on the right side and allow you to choose what limitations will your friend have while working on your project. You can choose between "Can Edit" and "Can View".

### Share Settings
If you're worried about the sanctity of your code after grant access to other developers, fear not. You can always take a look at a File Revision history to view line-by-line changes made to your project over time. The Share can be removed by right-clicking the file/folder in you File Explorer and selecting the "Remove share" from context menu:

![](/images/share-remove.png)

In order to easily manage your shares, just go to your [Dashboard](#dashboard) and locate them under My shares.

![](/images/dashboard-myshares.png)

Also, here you can check who shared files with you under Shared with me.

![](/images/dashboard-sharedwithme.png)

* [Share Link](#share-link)
* [Pair Programming](#pair-programming)
* [SSH Realtime Collaboration](#ssh-realtime-collaboration)

## Share Link
To share files with anyone, simply right-click on Project, Connection, Folder or even File in File Explorer and select the Share button.

Share Link is located on the top of the window, simply copy the Share link and send it to your friend or coworker and they can open the shared file by pasting the link in their browser:

![](/images/share.png)

## Pair Programming

If you wish to pair code with other users, you must first enable "Pair Programming" option in User or Project Prefrences

![](/images/pairprogramm.png)

Now, all users which have access to your shared files and have this option enabled as well will see each other cursors in the real time.

![](/images/share-editing.png)

You can see who is currently working on the file by the initials in top-right corner of the screen, and if you hover over it will display the email of the user:

![](/images/share-toprightcorner.png)

## SSH Realtime Collaboration
You shared your project and you want to give that user SSH access so you can collaborate from there? No problem! Select that connection and press share in top menu bar afterwards.

![](/images/shareicon.png)

Please keep in mind that your SSH should be open. Your collaborator will receive a notification in top right corner that says: "user@mail.com has requested SSH terminal session collaboration on connection name_of_connection with you".

## Revisions

Every time you save a file on Codeanywhere, a diff of any changes made to it is saved by the server. Over time, you can view these file revisions as content is added and removed from your files. You can also restore a file to any previously saved state; you'll never have to worry about losing your work ever again! To access file revisions, you simply click on revision button located in toolbox above Codeanywhere Editor.

![](/images/revisions.png)

This will open the Revisions History panel.

Once you select the revision you want, the "Compare window" appears:

![](/images/revisions-fix.png)

In Compare window you can see the changes between current file and saved revision. Pressing the arrow key "><" you can transfer the code from revision to your file and once you are done with editing, simply press the "Save" button at the bottom to confirm your changes.

## Mini Map
A MiniMap is like a wider scroll bar in which you see a mini version of the entire file you’re working on. It is a very user productive feature as it allows you to scroll through your file with speed and ease by using the compressed image of your text on the upper right hand corner. MiniMap will be enabled to all our users by default. In case you don’t want to use MiniMap, you can disable it by doing the following: View -> MiniMap

![](/images/minimap.png)

and making sure MiniMap option isn’t checked. Of course, you can re-enable it at any time by the same method

## Searching and Replacing in Editor
### Quicksearch
Quicksearch can be activated by hitting Cmd-F on a Mac, or Ctrl-F on a Unix/Windows machine. As you type in the quicksearch bar, the code with the matching text is underlined, and if you want to move between the matching results you can use the arrow keys on the right side which will instantly shift you to the next available result. This is a great way to quickly search around in your code without hassle.

Quicksearch offers the following options: ● Regular Expressions: when enabled, your search is treated as a regular expression ● Match Case: when enabled, your search is case sensitive

### Search and Replace
Building on the features of quicksearch, search and replace allows you to replace segments of code in your file. Replacing offers two options like quicksearch: ● Match Case: when enabled, your search is case sensitive ● Regular Expressions: when enabled, your search is treated as a regular expression

If you don't want to use keyboard shortcuts, the find feature is also located on top of File Explorer and is represented by magnifying glass icon and the "Find" text.

![](/images/find.png)

## Find in Files
Find in files is a quick way to see if a certain string or pattern appears across many files.

This feature works for containers and SSH connections.

To initiate Find in Files, go to the Find menu, then Find in Files or use the keyboard shortcut (Cmd/Ctrl + Shift + F).

![](/images/fif.png)

Find in Files can also be initiated using File Explorer by opening context menu for a directory:

![](/images/fifcontext.png)

When this is done, a find bar will show up:

![](/images/fifbar.png)

### Find
To start a search, type the search term or string into the "Find" text box and click Find or press Enter. A window will open below the find panel that will show all occurrences of the search terms. To go to the file where the search term occurs, simply click the search result text.

### Path
If you want to narrow down your search, you can specify a path to a directory you are interested in.

### Exclude
Exclude field can be used for skiping any file with a name suffix that matches the pattern glob, using wildcard matching.

### Search Modifiers
Regular Expressions - Turning this on allows for use of regular expressions which are complex but can help match very specific patterns of strings

Match Case - If the search will be case sensitive or not

## GoTo
### GoTo Files
In order to search across a set of files, you'll want to use the Goto Files feature. Here, you can search of a string or regular expression, within your entire File Explorer. You can also filter based on extensions, like .html or .php.

In your Top Menu Bar, you can find a GoTo option. With it, you can check all the options for easier search!

![](/images/goto.png)

### GoTo Anything
Shortcut for this function is, for Mac, CMD + P, or, for Windows, CTRL + P. After you start typing the name of your file/folder, you’ll be able to activate it without any hustle!

### GoTo Commands
Shortcut for this function is, for Mac, CMD + Shift + P, or for Windows, CTRL + Shift + P. This feature will enable you to go to feature you can use with Codeanywhere!

### GoTo Line
Shortcut for this function is, for Mac, CMD + G, or for Windows, CTRL + G. You can go to any line in your currently opened file!

## Character Encoding
When the file is opened you can set the encoding which will be used when saving the file. You can access the encoding menu by clicking CTRL + P, on Windows, or CMD + P, on MAC, and entering "$Encoding". Here's the list of all supported encoding:

* ASCII
* Big5
* EUC-KR
* GB2312
* KOI8-R
* CP1256
* ISO-8859-1
* ISO-8859-2
* ISO-8859-3
* ISO-8859-4
* ISO-8859-5
* ISO-8859-6
* ISO-8859-7
* ISO-8859-8
* ISO-8859-9
* ISO-8859-13
* ISO-8859-14
* ISO-8859-15
* JIS
* Windows-1250
* Windows-1251
* Windows-1252
* Windows-1253
* Windows-1254
* Windows-1255
* Windows-1256
* Windows-1257
* Windows-1258
* UTF-7
* UTF-8
* UTF-16
* UTF-32

## Multiple Licenses

If you’re managing a huge number of employees, or if you are just a small team, Codeanywhere’s feature Multiple License, enables you to manage your entire team accounts, including which plans, add-ons and permissions they have.

![](/images/multiplelicense.png)

Once you have set up and upgraded your primary Codeanywhere account to a Premium Plan, you can easily add additional accounts over which you have complete control. Management of this feature is done through your [Dashboard](#dashboard) by purchasing an Addon and it consists of creating new, or adding existing accounts under your management, granting of add-ons and, if necessary, closing the accounts.

## Preview Files
To preview a file you can click on a "File Preview" icon while file is open

![](/images/previewfile.png)

Or you can right click on a file in the file tree and then click "Preview"

![](/images/previewfiletree.png)

### Setting up preview file parameters
#### Remote connections (FTP, SFTP, FTPS, SSH)
You can setup preview parameters while adding a new remote connection, or you can edit the existing connection. To edit existing connection, right click on a connection and click settings

You should see popup like this

![](/images/connectionconfig.png) 

Parameters Root Directory and Web URL are required to preview a file.

Root directory is the directory from which your site is served (e.g. './' or '/var/www/html')

NOTE: Root directory needs to be in the same format as initial dir, if initial dir contains absolute/relative path so should Root directory too

Web URL is base URL of your server (e.g. '[https://myserver.com](https://myserver.com)')

#### Containers
Codeanywhere gets preview file information from Container's config file. Base preview URL is defined from run[0].preview.url property of config file. Preview root dir is by default '/home/cabox/workspace'. If you want to change preview root dir, you can define property run[0].preview.path. Make sure that path is in absolute format, and it will calculate the URL relative form '/home/cabox/workspace'.

## Two Factor Authentication

When you are logging into your account using only your username and password, or any of our oAuth methods, it is considered a single factor authentication. Two factor authentication adds a second level of authentication to an account log-in by sending additional set of numbers to your mobile device when first logging to your account from some new device!

At Codeanywhere, we decided to provide our users with 2FA, in a way to use SMS to deliver that second factor of authentication because it is considerably universal - all you need is a mobile phone to receive your login code! You can set everything up in your Dashboard under Billing!

![](/images/2fa1.png)

![](/images/2fa2.png)

After turning this feature on - enter your mobile number:

![](/images/2fa3.png)

And that’s it! You’ll be prompted whether you’d like to trust your current device, so you don’t have to enter your code each time you want to log in!

It definitely pays off to be a little patient and spend some extra time to ensure that all of your data is under high level of security! Now you can be sure that all the codes you’ve been working on will remain safe and sound! This feature is only available on Freelancer Plan and higher!

## Bookmarks
To easily navigate in large files you can use Editor bookmarks. Bookmarks are tied to the line so if you delete or add new lines it will move the bookmark as well.

Bookmarks shortcuts:

* Toggle bookmark (Cmd-F2)
* Jump to next bookmark (F2)
* Jump to previous bookmark (Shift-F2)
* Clear bookmarks (Shift-Cmd-F2)

All shortcuts can be changed using [Key Binding Preferences](#key-bindings)

## Open Files
At the top of the Explorer is a section labeled Open Files. This is a list of active files or previews.

![](/images/openfiles.png)

With Open files feature, you can:

* Switch between files
* Close files
* See currently active file
* Check which files are unsaved

You can also disable or enable this feature by using [General Preferences](#general)

## Vim Mode
If you want to use Vim keybindings in your Codeanywhere, you can enable them in "General preferences":

![](/images/generalprefs.png)

When enabled, in "normal vim mode" you should see a green thick cursor like the one below:

![](/images/vimcursor.png)

"command-line vim mode" can be opened using the ":" key:

![](/images/vimcommand.png)

### Features

* All common motions and operators, including text objects
* Operator motion orthogonality
* Visual mode - characterwise, linewise, blockwise
* Full macro support (q, @)
* Incremental highlighted search (/, ?, #, , g#, g)
* Search/replace with confirm (:substitute, :%s)
* Search history
* Jump lists (Ctrl-o, Ctrl-i)
* Key/command mapping with API (:map, :nmap, :vmap)
* Sort (:sort)
* Marks (`, ')
* :global
* Cross-buffer yank/paste


## Distraction Free Mode

If you want to use Codeanywhere and focus only on your code, you can enable "Distraction Free Mode", which hides all UI except the editor.

To enable it, use one of the following options:
* Main menu (View -> Distraction Free Mode)
* key shortcut (Shift-F11 for PC or Cmd-Ctrl-Shift-F for mac)
* "Goto Anything -> Enable Distraction Free Mode"

![](/images/distractfree.png)

To disable it, use one of the following options:
* the "Esc" key
* key shortcut (Shift-F11 for PC or Cmd-Ctrl-Shift-F for mac)
* "Goto Anything -> Disable Distraction Free Mode".
