== How to Install TaskLocale ==

NOTE: These steps assume that ~/bin is included within your PATH environment variable.

1. Compile Taskwarrior for your language of choice. Besides English, it supports German, Russian, French, Japanese, Portuguese, Spanish, Italian, and Polish.

2. Execute the following commands:
	cp -R dottaskslashtasklocale ~/.task/tasklocale
	cp tasklocale ~/bin

3. Edit ~/.task/tasklocale/taskrc, changing the default language reference (epo-RUS) to the language reference of your choice. The only language currently supported is Esperanto.

4. Edit ~/.taskrc, adding the following line:
	include ~/.task/tasklocale/taskrc

5. Create a symbolic link for your language's word for "task", if you like.
	Esperanto: ln -s tasklocale ~/bin/tasko


== How to Use TaskLocale ==

TaskLocale is merely a localization wrapper for Taskwarrior, so usage is the same as using Taskwarrior, except that inputs are understood in your own language.

To see localized list of commands, column names, and date references, run the following commands:
	task _aliases
	tasklocale _columns
