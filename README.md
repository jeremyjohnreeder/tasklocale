== How to Install TaskLocale ==

NOTE: These steps assume that ~/bin is included within your PATH environment variable.

1. Compile Taskwarrior for your language of choice. Besides English, it supports German, Russian, French, Japanese, Portuguese, Spanish, Italian, and Polish.

2. Execute the following commands:
	cp -R dottaskslashtasklocale ~/.task/tasklocale
	cp tasklocale ~/bin

3. Create a symbolic link to your language of choice, such as epo-RUS.
	ln -s epo-RUS ~/.task/tasklocale/locale

4. Edit ~/.taskrc, adding the following line:
	include ~/.task/tasklocale/taskrc

5. Create a symbolic link for your language's word for "task", if you like.
	Esperanto: ln -s tasklocale ~/bin/tasko


== How to Use TaskLocale ==

TaskLocale is merely a localization wrapper for Taskwarrior, so usage is the same as using Taskwarrior, except that inputs are understood in your own language. More specifically, localized equivalents of the following are understood:
	- commands
	- column names
	- month names and standard abbreviations
	- day names and standard abbreviations
	- miscellaneous time references:
		- now
		- tomorrow
		- easter
		- someday
	- true and false
	- yes and no

Localized equivalents of time-period references such as "2wk" are not supported. ISO-8601 time-period references such as "P2W" are recommended.

To see a list of supported commands, columns, and time references in your language of choice, run the following commands:
	tasklocale _commands
	tasklocale _columns
