# My gh alias

This README is an attempt to collect interesting alias for `gh` in the context of education.

The idea is to have a section for user.


## crguezl

My two most important alias are 

1. `gh cd` to change the default organization and 
2. `gh pwd` to see what is my default organization

Here are my alias:

```
➜  gh-alias date
miércoles,  2 de febrero de 2022, 10:33:29 WET
➜  gh-alias gh alias list
cd:                            !gh config set current-org "$1" 2>/dev/null
pwd:                           !gh config get current-org
co:                            pr checkout
create-repo:                   !gh api https://api.github.com/orgs/$2/repos -X POST --field name=$1
get-labs:                      api /search/repositories?q=$1+org:$2+in:name
get-r:                         api /orgs/$1/repos
get-repos:                     api /orgs/$1/repos
org-list-names:                api --paginate /user/memberships/orgs --jq '.[].organization.login'
orgs-list:                     api --paginate /user/memberships/orgs  --jq '.[].organization | .login, .url'
add-todo:                      issue create -R crguezl/todo -p todo -a @me -t "$1" -b "$1" -w
branch-delete:                 !git push $1 :$2
browse-graphql:                !open https://docs.github.com/en/graphql
browse-rest-api:               !open https://docs.github.com/en/rest
browse-settings:               !open https://www.github.com/settings/
browse-tokens:                 !open https://www.github.com/settings/tokens
repo-delete:                   api -X DELETE "/repos/$1"
repo-issues-template-example:  !gh api repos/$1/issues --template "$(cat ~/.local/share/gh/templates/template.gotemplate)"
todo:                          !open https://github.com/crguezl/todo/projects/1
upgrade-org:                   !open  https://education.github.com/toolbox/offers/github-org-upgrades
user-orgs:                     api --paginate /user/memberships/orgs
user-repos:                    api --paginate /users/$1/repos
```