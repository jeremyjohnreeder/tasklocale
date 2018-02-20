== How to Install TaskLocale ==

NOTE: These steps assume that ~/bin is included within your PATH environment variable.

1. Execute the following commands:
	cp -R dottaskslashtasklocale ~/.task/tasklocale
	cp tasklocale ~/bin

2. Edit ~/.task/tasklocale/taskrc, changing the default language reference (epo-RUS) to the language reference of your choice.

3. Edit ~/.taskrc, adding the following line:
	include ~/.task/tasklocale/taskrc


== How to Use TaskLocale ==

TaskLocale is merely a localization wrapper for Taskwarrior, so usage is the same as using Taskwarrior, except that inputs are understood in your own language.

To see localized list of commands, column names, and date references, run the following commands:
	task _aliases
	tasklocale _columns
