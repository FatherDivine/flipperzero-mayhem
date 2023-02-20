There ain't no such thing as a [free lunch](https://en.wikipedia.org/wiki/There_ain%27t_no_such_thing_as_a_free_lunch). If you want a better portapack, there is no better way to get it than collaborating.

# Write documentation

There is a lot of missing documentation about all the features, so it is really important to write clean and detailed instructions for them. In this current wiki, you can modify or add new content with a normal Github account. 

For learning about the text formatting, check the [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

# Coding new stuff or fixing bugs

I know what are you thinking: "I am not an expert, I do not know C++, I am not capable, etc", but nobody really is until they do. The easiest way to get a bug fixed or a new feature is to code it yourself.

So, setup the environment and compile the code as instructed below. Modify something dumb: add some text, change a message, ... compile again and test. Try to understand how things works; this is exactly how everyone gets involved. 

> While you learn, you can add comments and rename variables if you think it will help others to understand the code. **This is also a very appreciated contribution.**

## Environment setup

### Fork the repository
1. Download and install [Github desktop](https://desktop.github.com/)
2. Log to Github, open the [repository](https://github.com/eried/portapack-mayhem) and click **Fork** on the top right
3. In your Fork, Click **Clone** and **Open in Desktop**
4. Follow the rest of instructions in Github desktop

### Prepare for compilation
1. [Compile your fork](Compile-firmware)

### Work on the code

It is recommended to work in [branches](https://help.github.com/en/desktop/contributing-to-projects/creating-a-branch-for-your-work), but as a beginner, it is ok to work on your master branch. 

Create [commits](https://help.github.com/en/desktop/contributing-to-projects/committing-and-reviewing-changes-to-your-project) with your changes after you complete them. 

Just keep in mind:
* Keep it simple, the fewer commits, affected files and lines, the better
* Use a descriptive name for the commits, add the URL of the issue if you were fixing something specific
* The project needs to compile successfully after each commit

### Submit your changes
This is the last stage. Your new feature or fix is ready and this is how you submit the changes:

1. Publish the branch (if necessary) and push all the commits
2. Do a [pull request](https://help.github.com/en/desktop/contributing-to-projects/creating-an-issue-or-pull-request). Use a descriptive title and description if you think is necessary
3. Just follow the interaction on Github now