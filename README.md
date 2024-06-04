![how-to-guide](https://github.com/perceptronbd/how-to-guide/assets/53243993/3d3e08ad-b0e1-47b6-85ad-9eed580f92dd)

# GitHub Collaboration Guidelines

Please follow these guidelines to ensure a streamlined and efficient collaboration process on our GitHub repositories:

### 1. Repository Setup
Clone the repository: Obtain the repository by executing the following command in your terminal:
```
git clone [repository-url]
```

### 2. Issue Assignment
Review the issues, project board, or issue tracker (Jira) to identify the issue assigned to you.

### 3. Branch Creation
Create a new branch for the issue you'll be working on, following the branch naming convention: `b-[issue_title]` <br />
Example: If your assigned issue title is `admin feature`, create a branch named  `b-admin-feature` <br />
Here is a step-by-step example:
1. View the issue and click on **“Create a branch”** under the Development section.![image](https://github.com/perceptronbd/how-to-guide/assets/53243993/065afa47-648d-4d15-8e2f-57a972351ee1)
2. Change the branch name to `b-[issue_title]` in this case, `B-demo-issue` since the issue number is #1.![image](https://github.com/perceptronbd/how-to-guide/assets/53243993/72811ce4-9d43-416b-af60-31ca21463d1e)
3. Click on “change branch source” and select the required branch, in this case, “Development”, and click “Create branch”. (make sure to have the checkout locally option checked).
4. And finally, run these commands in your local repo.
   ```
   git fetch origin
   git checkout B-demo-issue
   ```				

### 4. Commit and Push Changes
- Commit your changes with a clear and descriptive commit message.
- Push your branch to the remote repository:
 ```
  git push origin B-[issue_title]
 ```
**Tip:** Commit every change for better history readability.

### 5. Pull Request Submission
1. Once your changes are complete and pushed to your branch, create a pull request (PR) to merge your branch into the  `main`  branch (or the designated target branch).
2. Provide a detailed description of the changes made, referencing the issue name in the PR title and the issue number in the description.
Here is an example:
  - Here the Issue name/title is quiz and the number is #6 ![image](https://github.com/perceptronbd/how-to-guide/assets/53243993/16308b17-8c82-4bfe-bca4-48c42ea0ebf4)
  - The PR should look like this: Here provide the title of the issue in the title of the PR and in the description use keywords such as `close closes closed`,`fix fixes fixed` or `resolve resolves resolved` ![image](https://github.com/perceptronbd/how-to-guide/assets/53243993/006b8753-20eb-4ba5-9002-b031eaad4225)
  - Add more details in the issue description if necessary.

### 6. Important Note: 
- Before starting work on a new issue, ensure you have the latest changes from the  main (or target) branch by executing:
  ```
  git checkout main 
  git pull origin
  ```
Then, create a new branch as outlined in Step 3.
- In case of spikes (small changes that do not have an issue), create a branch with the naming convention of `[feature/change]-spike`.
  - For example: if the user feature requires some minor changes and does not require an issue then the branch name should be `user-feature-spike`

# VSCode Extension Setup

### Setup Workspace
- Create a .vscode in your workspace/root directory of the file you are working on.
- Create a settings.json and paste this setting
   ```json
   {
  "editor.defaultFormatter": "rvest.vs-code-prettier-eslint",
  "editor.formatOnType": false, 
  "editor.formatOnPaste": true, 
  "editor.formatOnSave": true, 
  "editor.formatOnSaveMode": "file",
  "files.autoSave": "onFocusChange",
  "vs-code-prettier-eslint.prettierLast": false, 
   "editor.codeActionsOnSave": {
        "source.fixAll": "explicit",
        "source.fixAll.eslint": "explicit"
    },
    "[javascriptreact]": {
      "editor.defaultFormatter": "esbenp.prettier-vscode"
    }
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
![image](https://github.com/perceptronbd/how-to-guide/assets/53243993/ad54fdaa-1845-4cb7-a725-0738569b57d5)
![image](https://github.com/perceptronbd/how-to-guide/assets/53243993/386283e9-94c0-44bb-9946-2a138fb17dd4)

- **Prettier ESLint** extensions will format the code.
- **Todo Tree** extension will highlight the notes, docs, bugs, marks, etc.
#### How to use Todo Tree
Just start the comment with `NOTE:`, `DOC:`, `FIX:` etc to highlight the code or comment. ![image](https://github.com/perceptronbd/how-to-guide/assets/53243993/915ef0d4-62bb-4484-8f31-60de6413f57e) </br>
On the sidebar of the VSCode, open the extension to view the lists of the highlighted notes </br> ![image](https://github.com/perceptronbd/how-to-guide/assets/53243993/7d3aa54f-3e66-4fbc-be5b-c75747f45806)


Please adhere to these guidelines to maintain a well-organized and efficient collaboration workflow within our GitHub repositories.

`Happy Hacking!`

