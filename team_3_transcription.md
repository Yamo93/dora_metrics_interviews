H = host, G = guest (interviewee)

h: the purpose of the interview is to gather data on the dora metrics and software delivery performance. we want to check why is deployment frequency, low, high, and lead time for change.

h: the first question is, please exlpain your team structure. what does it consist of today?

g: today it's shrinking, but three months back, there were five developers. the tricky part is that the application has several components with different languages, so one developer was working in a different part of the project, so that made the collaboration difficult.

h: you mean different programming languages?

g: yes, we had two backends c++ and java, the frontend was javascript. the api services were python services.

g: the collaboration was bad and you could not help in a specific part. we had two business analysts back then, one ux designer, one tester, one scrum master.

h: the reason why we ask this is because we think that you need to take the whole team into the context.

h: please briefly explain your work process from sprint planning to release.

g: now that we are in hibernation, we switched to kanban. but before, we had sprint meetings, to break down epics into tasks, and i think that was useful. we did sprints for three weeks. when a sprint was finished, we promoted our release branch, we were working with git flow, so that release branch was tested for 2-3 weeks, manual testing, and then it was released to production

h: so you made one release per sprint kind of?

g: kind of, sometimes, or often, we made one release, but we had already finished the previous sprint, so we were just waiting for testing the previous sprint but we hadn't released the old sprints.

h: so you had pending releases?

g: yes! the releases were pending, and that's why we can see big lead times sometimes. until a change was released to production, it was at least 6 weeks.

h: the next question would be: how often was your aim to deploy to production?

g: the aim was one release per month, which i don't think is very good.

h: but it's understandable why, since it's a more complex setup.

g: yes, and it was a legacy setup, and not easy to change.

h: how do you wish the lead time for change to be?

g: a week.

h: one of the biggest questions we have, since we have asked some times now, and I looked into the answers you got from the teams, i thought of the fact that most of the teams, even if they collect the data, they don't look at it.

g: yes, and that's the same for us. there is only one team that is actively looking at the data.

g: what we have done is that most of the teams don't understand the data, so we might try to do some type of workshops with them.

h: so lack of understanding is a factor?

g: a bit of both, lack of understanding and what does that data provide for me?

h: yes, the value. people doubt the value.

g: if you look at it, it's not giving you any value. but if you want to deploy more often, then you can learn from that data and start analysing.

h: so, if you have a strategy and you want to do some change in the workflow, then you can follow up on the data to learn what strategies are successful.

h: if we look at the deployment frequency reports... (shows report) since you are also in the DevOps team, i would like to ask you questions about how we can understand it. we have something called average and median. what does the Y axis mean for a given point of time? the Y axis is the number of Jira Ids per week and reason. but I am questioning, do we look at the frequency of deployments, or the volume of deployments?

g: usually the frequency, in the Y axis you may have deployed 30 or 40 Jira Ids, but in DORA metrics you should look into the number of releases.

h: if you can briefly explain the highs and lows of the graph, what do you think can impact this?

g: the bigger numbers are the normal releases after a sprint, the spike is that we have an issue in reporting, and we had an issue with how we report the data, because we usually did several releases to pre-production, and then we deployed one specific version to production, and we lost changes in the process.

h: so there is some loss of data?

g: yes, there is loss of data, but we can see that the bigger numbers are the normal releases, and when it goes down it's a hotfix or similar, and that's why they have fewer issues. and if we look at the lead time, it should be shorter.

h: how do I know how often a team releases? do I look at the weeks?

g: so at week 19, there was maybe a release of 3 years, and during week 24 there was a release of 25 issues, and so on.

h: so this means that you are deploying quite often?Ä

g: yes, because we have many issues.

h: so what is happening with the omitted weeks?

g: that can be confusing, since it is not only data for the application but also for the backend. probably, the backend deployments are also included in this.

h: do backend deployments affect end users?

g: no, it's more internal. we have specific dashboard where we can distinguish between them, but that's why we are seeing more data than in reality.

h: thanks, I think I have good answers.

h: if we go to lead time for change then (shows reports)...

g: yes, as i said, one release is waiting for another, usually a sprint is 21 days.

h: but the median? you are meeting expectations, or is it too high?

g: yes, it's too high. the aim is weekly, 7 days, but now it's above that. it's even above a sprint, since a sprint is 21 days.

g: that's interesting, because before looking at this graph, I thought that we had a very high lead time.

g: for week 42, we had a hotfix, but again, i don't know if we are mixing backend with frontend data. that's one of the challenges that we had, that we have the main application, and then we have all the repositories with components like the backend, the services, and so on. we have a specific dashboard where we can distinguish between them. because of course, the backend doesn't have the release cycle that the frontend has. for one of the applications, if we finish a sprint and we are doing two weeks of manual testing, if an issue is found during those two weeks, then we have to go to that release, patch it through git flow.

h: could that potentially postpone the release?

g: yes, exactly. it happens. we tested something that we had developed a month ago, so we don't even remember what we did then.

h: those are pretty much the questions I had, and you gave good answers. this data will be transcribed, we will look at it and then we will interview another team this afternoon and ask them the same questions. I think that they have better data.

g: most of the teams have nice lead time and deployment frequency, but most of the teams - and this is a spoiler - are struggling with translations.

h: is there any way around that?

g: it's tricky, the problem is that you can not deploy something for all countries if you only have english as language. maybe the automatic translations are fine sometimes, but they need some manual touch.

h: is it possible to automate the translation for a period of time, and then it can be fixed afterwards?

g: yes, that is a possible solution. I heard that in all of the teams, they have developed something, but they have to wait a week or so to send the translations to the countries. if they are releasing every week, probably they concentrate the translations.
