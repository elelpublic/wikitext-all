wikitext-all
============

Compile the mylyn wikitext sources into one jar. Add a gradle build system.

Why?
----

Mylyns wikitext is a great effort to parse and format wiki syntax and create html pages. Also it allows for extensions with your own wiki languages. Read more here: <http://wiki.eclipse.org/Mylyn/WikiText>

But it is a little hard to use, since there is no maven-, ivy- or gradle repo to pull it as a dependency.

Also there is no git repo.

This project does nothing more than to add a gradle build, so you can create one jar to use in your projectes. Also obviously it is a git repo.

Todo
----

I have not yet come around to publish the artifact somewhere central. If you can help me with this, I'd appreciate it very much.

How?
----

This is the cycle I have to go manually to get a new release working here.

  * Download Mylyn Wikitext Standalone here: <http://www.eclipse.org/mylyn/downloads/>
  * Remove some stuff (see below)
  * Copy the remaining files into this project
  * Try to build: `gradle build`
  * Fix anything that's broken (new dependencies, new folders, new files, removed stuff, ...)
  * Commit and push to github: https://github.com/elelpublic/wikitext-all.git
  
### Remove some stuff

We remove the pre built aritfacts in the downloaded project:

		rm *.jar
		
Build
-----

You build of course with your standard...

		gradle build
		
... and find your all in one wikitext-*.jar in `build/libs` . 

  
 
  
 
