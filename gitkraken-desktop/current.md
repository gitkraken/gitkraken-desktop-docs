---

title: GitKraken Desktop Release Notes
description: View a history of the new features and fixes in GitKraken Desktop's Version 11.
og_image: /img/GitKrakenClient-Hero.png
taxonomy:
    category: gitkraken-desktop

---

Behold the evolution of GitKraken Desktop! Find out what&rsquo;s new, what&rsquo;s fixed, or just take a trip down memory lane with a nostalgic swagger, remembering those bugs of yesterday.

<a href="https://www.gitkraken.com/download?product=gitkraken&source=help_center" target="_blank" class="button button--basic ">Download Current Version Now</a>

Check out our [GitKraken Roadmap](https://www.gitkraken.com/git-client/roadmap?product=gitkraken&source=help_center) to see what we’re working on.
***

<a id="v11-1-0"></a>
## Version 11.1.0
<kbd>>Tuesday, May 6th, 2025</kbd>

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/jg3n_dg4IjM?si=87vB8ooSU5GAn5wk" frameborder="0" allowfullscreen></iframe>
</div>
 
_"More Jarvis. Less Skynet."_

### New ✨
 - **GitKraken AI:** New AI-powered capabilities to accelerate your development workflow, with expanded support for additional providers and environments.
   - Pull Request Title and Description Generation
     - Generate titles and descriptions for Pull Requests based on the commits of the PR in just a click.
     - When creating a Pull Request, click `Generate title and description` to automatically populate the fields using GitKraken AI.
     - If you have a Pull Request template selected, GitKraken AI will attempt to generate content that adheres to the selected template.
   - Stash Message Generation
     - Generate stash messages based on your code changes in just a click.
     - With a WIP selected, click on the sparkle icon in the stash message form to have GitKraken AI generate a stash message based on your staged changes.
   - Amend Commit Message
     - You can now also generate a new commit message when amending a previous commit message.
   - Expanded provider support when using your own API key
     - Added support for OpenAI GPT-4.1 models.
     - Removed the deprecated OpenAI o1-mini model.
     - Added Google Gemini as a provider.
     - Added Azure as a provider (private AI model providers such as Azure require GitKraken Advanced).
     - You can now configure a custom URL endpoint for an OpenAI compatible API to use with GitKraken AI, like a local or self-hosted AI server.


### Improvements 🙌
 - You can now Hide All / Show All items in the Local and Remote sections of the Left Panel from each section header's context menu.
    - The Hide All / Show All actions for Tags and Stashes have also been moved to their respective section headers.
 - GitHub user avatars will now display in the Commit Graph and Commit Details Panel for commits made on GitHub repositories.
 - Experimental Feature - Git Executable:
   - Respects `core.commentString` and `core.commentChar` values from your Git config.
   - Improved stability and performance for on-premise clients when authenticating with Git remotes.
 - Conflict Prevention:
   - Potential conflict alerts with your teammates will now work when the current branch has no upstream.
   - You can now access the branches involved in a potential conflict directly from the menu, and each branch label matches the color of the branch in the Commit Graph.
 - Upgraded Electron to v34.

### Bug Fixes 🐛
 - The Repository Management tab now displays GitLab workspaces with more than 25 repos.
 - Fixed an issue in the graph where branch labels wouldn't render properly.
 - Fixed several styling issues across the application.
 - Experimental Feature - Git Executable:
   - Fixed an issue where Pull failed with files having the same name but different casing in a case-insensitive file system.


***
<a id="v11-0-0"></a>
## Version 11.0.0
<kbd>Monday, March 31st, 2025</kbd>

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/sVLftA_jpak?si=87vB8ooSU5GAn5wk" frameborder="0" allowfullscreen></iframe>
</div>

_"Turn it up to 11! 🎸"_

### New ✨
 - **GitKraken AI:** A seamless extension of your development workflow, [GitKraken AI](https://help.gitkraken.com/gitkraken-desktop/gkd-gitkraken-ai/) automates tedious tasks to improve your efficiency and focus.
   - Commit Message Generation
     - You'll now be able to generate clear, meaningful commit messages based on your code changes in just a click.
     - With a WIP selected, click on the sparkle icon in the commit message form to have GitKraken AI generate a commit message for you based on your staged changes.
   - Explain Commits
     - You can now get detailed summaries of changes made in your repository without spending time diving through files and diffs.
     - With one or multiple commits selected in the Commit Graph, click on the `Explain` button in the top right of the Commit Panel to generate an explanation of changes made in the selected commits.
   - Configure GitKraken AI from _Preferences > GitKraken AI_
     - Use the `Custom Instructions` setting to provide additional details so GitKraken AI can better tailor commit messages and explanations for you.
     - With GitKraken AI enabled, you can also select to use your own API key to make requests directly to OpenAI or Anthropic. When one of those providers is selected, you can choose what model you'd like to use for each AI feature.
     - Note: The AI Commit Message Generation section has been removed from _Preferences > Experimental_.


### Improvements 🙌
 - We updated our plans to better align with how developers and teams use GitKraken, and your new plan is now reflected in the status bar.
 - Upgraded React to v17.
 - Updated Git to 2.49.0.

### Bug Fixes 🐛
 - Launchpad now works with GitHub users set as Enterprise Managed Users.


