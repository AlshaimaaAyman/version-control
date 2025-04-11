# version control task 2
# Deleting Git Branches

1:-Delete a Local Branch
1.1-Safe delete:-  
git branch -d branch-name   

1.2:-Force delete
git branch -D branch-name     

2:-Delete a Remote Branch
git push origin --delete branch-name


# Annotated tags vs Lightweight Tags 
# Annotated tags 
Full object: Annotated tags are stored as full objects in the Git database, meaning they include more information like the tagger's name, email, date, and a message.
Recommended for releases: Since they contain metadata and are easier to associate with specific releases, annotated tags are often used for versioning and releases.
Can be signed: with GPG keys, ensuring integrity and authenticity.
Advantages:
Rich metadata: You get extra information, like the author and a message describing the tag.
Verifiable: Can be GPG-signed, providing more security and trust.
Best for releases: Typically used to mark official release points.

# Lightweight Tags
Simple reference: Lightweight tags are essentially just a reference (or pointer) to a specific commit. They don't store any extra information or metadata.
Advantages:
Quick and simple: Used for temporary or personal marks without needing to record additional data.
Faster: Because it doesn't store extra metadata, it's faster and more lightweight.
No message or extra data: It doesn't have the tagger's information, date, or a message; it’s just a simple pointer to a commit.


# When to use Rebase
Above illustration makes it look like that git rebase is essentially not good to work on public branches. However, git rebase can also be done on the same branch. By periodically performing an interactive rebase on local branch, you can make sure each commit mentioned in git history is focused and meaningful. This lets you write your code without worrying about breaking it up into isolated commits — you can fix it up after the fact. This process is also sometimes known as the local cleanup.

# How to list tags?
git tag
List with details: git show-ref --tags
List tags with patterns:- git tag -l 'v1*'
Show tag details:- git show <tagname>

# How to delete tag locally and remotely? 
1-Delete a Tag Locally:- git tag -d <tagname>
2-Delete a Tag  Remotely:- git push origin --delete <tagname>
3- Verify Deletion:-  
3.1 Locally:- git tag
3.2 Remotely:- git ls-remote --tags origin

# Add an image in the README.md file.
![My Image](images/img.jpg)

