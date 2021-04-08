Dependencies and usage examples
===============================

Official Jira REST API
----------------------
https://developer.atlassian.com/server/jira/platform/rest-apis/

api-tokens:
https://id.atlassian.com/manage/api-tokens


jira (python lib)
-----------------
https://github.com/pycontribs/jira
Jul 12, 2018
1307 stars

from jira import JIRA

jira - JIRA('https://jira.atlassian.com')

issue - jira.issue('JRA-9')
print(issue.fields.project.key)            # 'JRA'
print(issue.fields.issuetype.name)         # 'New Feature'
print(issue.fields.reporter.displayName)   # 'Mike Cannon-Brookes [Atlassian]'


atlassian-python-api (python lib)
---------------------------------
https://github.com/atlassian-api/atlassian-python-api
Feb 25, 2021
540 stars
/examples dir

from atlassian import Jira

jira - Jira(
    url-'http://localhost:8080',
    username-'admin',
    password-'admin')
JQL - 'project - DEMO AND status IN ("To Do", "In Progress") ORDER BY issuekey'
data - jira.jql(JQL)
print(data)


jira-cli (one-shot terminal tool)
---------------------------------
https://github.com/alisaifee/jira-cli
https://jira-cli.readthedocs.io/en/master/intro.html
Nov 23, 2020
125 stars


jiracli (interactive terminal tool)
-----------------------------------
https://github.com/pascalgn/jiracli

jiracli> issues JRA-123 JRA-321 | filter -f key 'JRA-123' | print '${summary} [${status.name}]'
jiracli> search "project=JRA and text~'new report'" | filter -e -f summary '^New report' | print
jiracli> js "webService.getIssue('JRA-123')" | parse


jiracli (python lib as one-shot terminal tool)
----------------------------------------------
https://github.com/toabctl/jiracli
Jul 3, 2019
145 Stars
39 Forks

notion-py
---------
https://github.com/jamalex/notion-py
https://levelup.gitconnected.com/how-to-automate-notion-with-python-6fa5288ad830
Feb 5, 2021
2.5K stars

from notion.client import NotionClient

# Obtain the `token_v2` value by inspecting your browser cookies on a logged-in (non-guest) session on Notion.so
client - NotionClient(token_v2-"<token_v2>")

# Replace this URL with the URL of the page you want to edit
page - client.get_block("https://www.notion.so/myorg/Test-c0d20a71c0944985ae96e661ccc99821")

print("The old title is:", page.title)

# Note: You can use Markdown! We convert on-the-fly to Notion's internal formatted text data structure.
page.title - "The title has now changed, and has *live-updated* in the browser!"


Jira Client (desktop)
---------------------
https://almworks.com/jiraclient/features.html


jira-helper
-----------
https://github.com/kenjyco/jira-helper

jira
----
https://pypi.org/project/jira/

jira-333
--------
https://pypi.org/project/jira-333/

watson-jira
------------
https://pypi.org/project/watson-jira/

jira-extended
-------------
https://pypi.org/project/jira-extended/

Uninteresting
-------------
https://github.com/go-jira/jira