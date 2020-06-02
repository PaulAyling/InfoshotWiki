INFORMATION ABOUT THE APP NAMING CONVENTION & GIT WORKFLOW

Semmantic Versioning of this app
https://semver.org/

1.      1.          0             
Major   Feature     Patch         feature name

Major Version Guidelines
0 : Prior to MVP
1 : Beta testing with limited users
2 : No user limitation


GIT PROCESS
How to conduct a merge of a feature on to the dev branch
1. Checkout release branch
2. Add tag to release branch update the tag with the semmantic version eg 0.4.0 Add users  
  3. Rebase changes into Dev
  4. manage merge conflicts
  5. confirm app is functional in new commit
  if app works{
    6. Make new commit of merge conflict 
  } else
  {
    6. git merge --abort
    7. Pull dev branch to get most recent
    8. Merge Develop into the feature branch
    9. Fix merge comflicts
    10. Resolve all conflicts
    11. commit all changes
    12. checkout Develop
    13. Merge feature branch to Develop
  }

  If you muck up a branch how to recover it to an earlier commmit
    if (commit = current) {
      [terminal] git merge --abort
    } commit = lastCommit {
      [sourcetree] reverse Commit
    } commit > lastCommit {
      [sourcetree] reset branch to this commit
    } commit > lastCommit && on pulling the remote branch overrites the local branch{
      [sourcetree] reset branch to this commit
     [terminal] git push --force origin develop
    }

  1. 
    git push --force origin develop 