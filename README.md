# GitHub API Integration

This repository demonstrates how to use the GitHub REST API to manage repository collaborators programmatically. The script focuses on fetching and displaying a list of users with specific access permissions (e.g., read access) without relying on the GitHub web interface.

---

## Features

1. **List Collaborators**: Retrieve and display a list of users with read access to a repository.
2. **Authentication**: Use a GitHub Personal Access Token (PAT) for secure API calls.
3. **Automation**: Simplify repetitive repository management tasks through scripting.

---

## Prerequisites

1. **GitHub Account**:
   - A GitHub account with necessary permissions on the repository.

2. **Personal Access Token (PAT)**:
   - Generate a token:
     - Go to **Settings > Developer Settings > Personal Access Tokens > Tokens (Classic)**.
     - Include the `repo` scope for repository access.
     - Save the token securely for use in the script.

3. **Repository Ownership**:
   - Ensure you own the repository or have admin rights to manage collaborators.

4. **Command-Line Tools**:
   - Install the following tools:
     - **`curl`**: For making HTTP requests.
     - **`jq`**: For parsing JSON responses.

---

## How to Use

### 1. Clone the Repository
Clone this repository to your local machine:

```bash
git clone https://github.com/<your-username>/github-api-integration.git
2. Configure the Script
Open the manage-access.sh script and configure the following:
bash
Copy code
USERNAME=<your-github-username>
TOKEN=<your-personal-access-token>
3. Run the Script
Run the script by providing the repository owner and repository name as arguments:

bash
Copy code
bash manage-access.sh <repo_owner> <repo_name>
Example:
bash
Copy code
bash manage-access.sh your-username github-api-integration
The script will output a list of users with read access to the specified repository.

API Overview
The script interacts with the following GitHub REST API endpoint:

List Collaborators: GET /repos/{owner}/{repo}/collaborators
For complete API documentation, refer to the GitHub REST API Documentation.

Limitations
Permissions:
The script requires admin privileges to fetch collaborator details.
Rate Limits:
API rate limits may restrict the number of requests you can make in a short time frame.
No Access Modification:
This script does not include functionality to modify or revoke collaborator permissions.
Example Use Case
If you're a repository owner or administrator and want to:

Audit collaborators with read access.
Simplify manual tasks by automating repository access checks.
This script provides an effective solution.

Repository Information
Repository Name: github-api-integration
Repository URL: https://github.com/<your-username>/github-api-integration
Please refer the script as well as the screenshot for the execution part
Feel free to fork, use, and contribute to this repository. 🚀


