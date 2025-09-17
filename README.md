# File-Permissions-in-Linux

The purpose of the File Permissions in Linux project was to audit and modify file permissions within a project directory to ensure proper security controls. This hands-on exercise helped me understand Linux file permission systems and apply the principle of least privilege to secure organizational data.

- Learned to use Linux command line tools (`ls -l`, `ls -la`, `chmod`) for file permission management.
- Understanding the 10-character permission string system for user/group/other permissions.
- Gained experience identifying security risks in file system permissions.
- Applied the principle of least privilege by removing unnecessary permissions from users and groups.
- Developed skills in managing both regular and hidden file permissions in Linux environments.

**Scenario:** Research team needed to audit file permissions in the projects directory to identify and remediate unauthorized access rights that posed security risks.

## Ref 1: Initial File and Directory Analysis
<img width="959" height="274" alt="Screenshot 2025-09-17 at 12 44 47 PM" src="https://github.com/user-attachments/assets/8b8ff870-f23c-4373-8034-ecfc2b468825" />
- Used `ls -la` command to check file permissions including hidden files
- Identified one directory named "drafts" and one hidden file ".projects_x.txt"
- Analyzed the 10-character permission strings for all files and directories
- Distinguished between regular files and directories in the output

## Ref 2: Permission String Analysis
<img width="975" height="871" alt="Screenshot 2025-09-17 at 12 50 38 PM" src="https://github.com/user-attachments/assets/6e22c848-a914-4619-85e2-08c0b3257572" />
- Analyzed the 10-character permission system structure
- Understood file type indicators (d for directory, - for file)
- Learned permission types: r (read), w (write), x (execute)
- Identified user categories: user (u), group (g), other (o)
- Example analysis: `.projects_x.txt` permissions `-rw--w----`

## Ref 3: Modifying File Permissions
<img width="943" height="227" alt="Screenshot 2025-09-17 at 12 48 33 PM" src="https://github.com/user-attachments/assets/c2e2ced4-b23c-4d64-9458-d7b8eebed289" />
- Removed write access from "other" users on project_k.txt file
- Used `chmod o-w project_k.txt` command to modify permissions
- Verified changes using `ls -l` command
- Applied organizational security policy preventing other users from having write access

## Ref 4: Hidden File Permission Management
<img width="1014" height="386" alt="Screenshot 2025-09-17 at 12 51 26 PM" src="https://github.com/user-attachments/assets/5eba5d1f-c7ee-4def-b5f1-e4c253ae03dc" />
- Modified permissions on hidden file `.projects_x.txt`
- Removed write permissions from both user and group
- Added read permissions to the group
- Ensured only user and group could read the file (no write or execute access)

## Ref 5: Directory Permission Control
<img width="1000" height="347" alt="Screenshot 2025-09-17 at 12 55 11 PM" src="https://github.com/user-attachments/assets/3fbd2521-5038-4c77-be97-d726ce2bd364" />
- Modified permissions on the "drafts" subdirectory
- Removed execute permissions from the group using `chmod g-x drafts`
- Ensured only the user (researcher2) has full read, write, and execute access
- Applied principle of least privilege to directory access

## Ref 6: Security Summary and Results
<img width="973" height="205" alt="Screenshot 2025-09-17 at 12 56 12 PM" src="https://github.com/user-attachments/assets/5f62d7c0-606c-45f4-886c-6ba8e48f130f" />
- Successfully implemented the principle of least privilege across all files and directories
- Secured organizational data by removing unnecessary permissions
- Demonstrated proficiency in Linux command line security management
- Created a more secure file system environment for the research team
