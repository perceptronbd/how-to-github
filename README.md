![how-to-guide](https://github.com/user-attachments/assets/081e9d71-b1b8-46cd-8de8-b98d3c4e4402)

# GitHub Collaboration Guidelines

## Types of Prefixes
- **feat**: A new feature
- **fix**: A bug fix
- **docs**: Documentation-only changes
- **style**: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc.)
- **refactor**: A code change that neither fixes a bug nor adds a feature
- **perf**: A code change that improves performance
- **test**: Adding missing tests or correcting existing tests
- **chore**: Changes to the build process or auxiliary tools and libraries such as documentation generation


### 1. Repository Setup
Clone the repository: Obtain the repository by executing the following command in your terminal:
```
git clone [repository-url]
```

### 2. Issue Assignment
Review the issues, project board, or issue tracker (Jira) to identify the issue assigned to you.

### 3. Branch Creation
Create a new branch for the issue you'll be working on, following the branch naming convention: `[type]/[issue_title]` <br />
Example: If your assigned issue title is `Login Feature for Admin`, create a branch named  `feat/admin` <br />
Here is a step-by-step example:
1. View the issue and click on **“Create a branch”** under the Development section. 
![Screenshot 2024-07-29 172356](https://github.com/user-attachments/assets/b6fc1e16-fa49-4b82-bfd8-4c70539780a6)
2. Change the branch name to `[type]/[issue_title]` in this case, `feat/login` since the issue number is about the "login feature for the user". 
![Screenshot 2024-07-29 172740](https://github.com/user-attachments/assets/7fb69f4c-7218-4edf-a603-8d395c0585e5)
3. Click on “change branch source” and select the required branch, in this case, "development”, and click “Create branch”. (Make sure to check the local checkout option.)![Screenshot 2024-07-29 172934](https://github.com/user-attachments/assets/fc468d62-2f51-4f9e-bb45-9ff2f8ebd89c) 
4. And finally, run these commands in your local repo.
   ```
   git fetch origin
   git checkout feat/login
   ```				

### 5. Write Clear and Concise Commit Messages
- **Subject Line:** Use a short, descriptive subject line (50 characters or less) that summarizes the change.
- **Body:** If necessary, add a more detailed explanation of what was changed and why. This is optional for small changes but recommended for complex changes.
- **Imperative Mood:** Write in the imperative mood. E.g., “Fix bug” rather than “Fixed bug”.
- And then push the changes to remote repo: ```git push origin [type]-[issue-title]```

### 6. Follow a Consistent Format
Here is a commonly used format:
- **Type**: The type of change being made (e.g., feat, fix, docs, style, refactor, test, chore).
- **Scope**: The area of the codebase the change affects (optional but helpful).
- **Subject**: A brief summary of the change.
- **Body**: A more detailed description of the change, if necessary.
Example:
```
feat(auth): add OAuth2 login support

Added OAuth2 login support to enable users to log in with   third-party services. 
- Integrated Google and Facebook login options 
- Updated the authentication service to handle OAuth2 tokens 
- Modified the login page to include new buttons

This change improves user experience by providing more login options.
```


### 7. Pull Request Submission
1. Once your changes are complete and pushed to your branch, create a pull request (PR) to merge your branch into the  `main`  branch (or the designated target branch).
2. Provide a detailed description of the changes made, referencing the issue name in the PR title and the issue number in the description.
Here is an example:
  - Here the Issue name/title is a quiz and the number is #6 ![image](https://github.com/perceptronbd/how-to-guide/assets/53243993/16308b17-8c82-4bfe-bca4-48c42ea0ebf4)
  - The PR should look like this: Here provide the title of the issue in the title of the PR and in the description use keywords such as `close closes closed`,`fix fixes fixed` or `resolve resolves resolved` ![image](https://github.com/perceptronbd/how-to-guide/assets/53243993/006b8753-20eb-4ba5-9002-b031eaad4225)
  - Add more details in the issue description if necessary.


# VSCode Extension Setup

### Setup Workspace
- Create a .vscode in your workspace/root directory of the file you are working on.
- Create a settings.json and paste this setting
   ```json
   {
   "todo-tree.general.showActivityBarBadge": true,
	"todo-tree.general.tags": [
		"NOTE",
		"TODO",
		"FIX",
		"MARK",
		"BUG",
		"DOC",
		"[ ]",
		"[x]"
	],
	"todo-tree.general.showIconsInsteadOfTagsInStatusBar": true,
	"todo-tree.general.statusBar": "tags",
	"todo-tree.highlights.defaultHighlight": {
		"type": "tag",
		"fontWeight": "bold",
		"foreground": "#d8d8d8",
		"opacity": 90
	},
	"todo-tree.highlights.customHighlight": {
		"TODO": {
			"icon": "checkbox",
			"type": "line",
			"background": "#65B741",
			"iconColour": "#65B741",
			"gutterIcon": true,
			"opacity": 0.5
		},
		"FIX": {
			"icon": "alert",
			"type": "line",
			"background": "#ffbb00",
			"iconColour": "#ffbb00",
			"gutterIcon": true,
			"opacity": 0.3
		},
		"DOC": {
			"icon": "book",
			"type": "line",
			"background": "#c8f1ff",
			"iconColour": "#c8f1ff",
			"gutterIcon": true,
			"opacity": 0.3
		},
		"NOTE": {
			"icon": "note",
			"type": "line",
			"background": "#00BFFF",
			"iconColour": "#00BFFF",
			"gutterIcon": true,
			"opacity": 0.3
		},
		"MARK": {
			"background": "#157EFB",
			"iconColour": "#157EFB",
			"gutterIcon": true,
			"opacity": 0.3,
			"type": "line",
			"icon": "tag"
		},
		"BUG": {
			"icon": "bug",
			"type": "line",
			"background": "#FE0000",
			"iconColour": "#FE0000",
			"gutterIcon": true,
			"opacity": 0.3
		},
		"[ ]": {
			"icon": "issue-draft"
		},
		"[x]": {
			"icon": "issue-closed"
		}
	  }
   }
   ```
   look into the repository for the setup.

### Install the Extensions
Install these two extensions: </br>
![image](https://github.com/perceptronbd/how-to-guide/assets/53243993/386283e9-94c0-44bb-9946-2a138fb17dd4)

- **Todo Tree** extension will highlight the notes, docs, bugs, marks, etc.
#### How to use Todo Tree
Just start the comment with `NOTE:`, `DOC:`, `FIX:` etc to highlight the code or comment. ![image](https://github.com/perceptronbd/how-to-guide/assets/53243993/915ef0d4-62bb-4484-8f31-60de6413f57e) </br>
On the sidebar of the VSCode, open the extension to view the lists of the highlighted notes </br> ![image](https://github.com/perceptronbd/how-to-guide/assets/53243993/7d3aa54f-3e66-4fbc-be5b-c75747f45806)

`Happy Hacking!`

