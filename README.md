   ```mermaid
%%{init: { 'logLevel': 'debug', 'theme': 'default' } }%%
gitGraph
   commit id:"27490bb"
   branch feature-one
   checkout feature-one
   commit id:"8b30c46"
   checkout main
   commit id:"4617141"
   checkout feature-one
   merge main
   checkout main
   commit id:"9f1ccd9"
   ```
   after
   ```
   git pull origin main
   ```
   with config set to 
   ```
   git config pull.rebase false
   ```
   we have merge commit and our git graph is look like so

  ```mermaid
%%{init: { 'logLevel': 'debug', 'theme': 'default' } }%%
gitGraph
   commit id:"27490bb"
   branch feature-one
   checkout feature-one
   commit id:"8b30c46"
   checkout main
   commit id:"4617141"
   checkout feature-one
   merge main
   checkout main
   commit id:"9f1ccd9"
   checkout feature-one
   merge main
   ```
