---
title: "Git Basics"
date: 2019-12-18
tags: [Git, devops]
header:
  image: "/images/cloud.png"
excerpt: "Git, devops"
---

## Your first commit





	hrishikesh$ ls
	first_file.txt
	hrishikesh$ 
	hrishikesh$ 
	hrishikesh$ git add .
	hrishikesh$ 
	hrishikesh$ 

 I'm basically saying, "Hey git, add all changes that are in the current directory."



Now when we tell Git to add the changes, it isn't actually tracking them yet. It hasn't made those permanent. In order to do that we need to commit them. So we use "git commit" and then a space and then we use -m, short for message, and then in quotes I'm going to put the message that I want to go with it. I'm just going to make it "Initial commit". So inside quotes, I've got my message so I'm now saying Okay, all those things you added and you're prepared to commit, now we want to actually commit them and track them, forever. So once I hit commit, it comes up and says, yep, you've made your commit, it gives me some information about it. This is the basic process we're going to be using over and over again with Git. 

 	hrishikesh$ git commit -m "initial commit"
	[master (root-commit) f193024] initial commit
 	  Committer: hrishikesh <hrishikesh@Hrishikeshs-MacBook-Pro.local>
	1 file changed, 2 insertions(+)
 	create mode 100644 first_file.txt
	hrishikesh$  