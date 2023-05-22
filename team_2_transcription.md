# Team 2 interview transcription

H = host
G = guest (interviewee)

H: the purpose of this interview is to gather data on the challenges in software delivery performance and identify strategies for deployment including time to market. it's about the dora metrics. first and foremost, if we just go through the questions.
can you please explain your team structure briefly? how many developers do oyu have?

g: we are currently three developers, one ux, half a qa engineer, she's on 50%, and one po (product owner).

h: can you explain your work process from sprint planning to release? from the beginning to the end of a sprint, how is the work usually done?

g: we are following kind of a loose sprint process. we never estimate anything. we never follow up on how much was completed within a sprint. so, the walls around the sprint are kind of loose. we often drag stuff into the sprint in the middle. the sprint concept for us is because it gives an overview on what we are working on. i have never worked with kanban, but i have heard from people that what we do is more kanban-like.

h: so you have sprint reviews, retros and so on?

g: yes, we have all of those scrum routines, so we have the retro, the refinement, and everything like that, but we're not super-structured when it comes to estimating and planning. we often do that continuously. around the release process, we kind of strive towards continuous delivery, so we try to always keep our main branch clean and releasable. it has changed a little bit since we got our QA engiener on 50% a few months ago, so now we are doing some integration testing and release testing as well. previously, when we had no dedicated QA engineer, we tried to do all of the testing in the pull request, but we have changed that slightly. the goal is to always release main, but we don't have any fixed, like releasing at the end of the sprint. we release whenever we think that it makes sense, and there is also some, like a factor with the translation that we need to take into account.

h: i read some of the devops team interviews with the other team, and the translation issue is a common thing.

g: yes.

h: how often do you deploy to production? you answered this already, so it's when it makes sense?

g: as often as possible, but we don't release like a single bug fix, because we don't have the automated release like another team has. it's a manual thing that we need to do, so we usually batch together a couple of features and push them out. but I think that we are averaging maybe twice a month or something.

h: ok. how often do you wish the taim to be from code commit to it running in production, lead time? what is your aspiration around that? or how do you think about it?

g: are we talking about code commit on main, or on any feature branch?

h: the way lead time for changes works is that it can be any pull request until that reaches production. if it doesn't reach production then it's not included, like if the PR is closed for some reason. how long do you wish that time to be, or do you even consider that in the team?

g: no, i wouldn't say that we do, because we often open PRs as drafts as well, to be able to have an early discussion, when everything is not... and that maybe comes back to our process, that we don't work with very detailed requirements in the Jira tasks. so when you pick up a task, it's not like you know exactly what needs to be done, but we work more investigative or whatever you say, it's an ongoing discussion between dev, and UX, and sometimes the PO as well. i think that for us, that measurement doesn't really make sense with the process that we have.

h: interesting, that's a really interesting take I think. the DORA metrics assume that you should work in a very concrete way, like pick a task, implement, test, release, and pick a new...

g: yes, for it to make sense you kind of need to know what to do from the first commit, and we will often not know that.

h: that makes sense! so, the next question is: do you regularly look at DORA metrics? how do you act accordingly? and if not, what may be possible reasons for not looking at it?

g: no, I don't. I tried to look at it a coupel of times in the past, but i have a hard time understanding the graphs i were seeing. i couldn't really relate the numbers to what we had been doing the previous few weeks. maybe there is an issue wit hhow we report it, or i am just not used to the power bi interface, i am not sure. but we haven't dug into it more. it's not a problem that we haveb rought up during hte retros, that we need this data, but it has just been fallen between chairs, it has not been prioritised to look at why the data doesn't make sense or how to interpret it.

h: yes, because i thought that we could look at it together briefly. (shows report) I had an interview with a developer from team 3, and their report looked really bad, and he explained why it looked like that. he felt that your report was good. I asked him about the Y axis, because to me it looks more like deployment volume rather than frequency. it looks like how many jira ids are deployed per week. have you looked at this, and do you have any explanation of this? what comes to your mind when you look at a report like this?

g: so this is supposed to give us the number of jira ids deployed to production per week? so for it to be over 0, we would have to do ta release that week, otherwise it would be 0?

h: that's what i think... you mentioned that you don't deploy every week.

g: yes...

h: so i don't know how to explain it, is there a loss of data? it's difficult to understand this graph, it doesn't make much sense to me.

g: this would mean that since week 44 last year, we have released at least once a week except for week 13?

h: yes...

g: that's not true. we definitely haven't released every week in that timespan between week 44 and week 13. but there is also some weeks missing, like week 48 isn't there. but aha, could it then be that the line actually starts at 1? so the weeks that are missing are weeks where there is no release?

h: could be, yes... so like week 5 is missing for example, so you didn't deploy anything week 5? does it mean that you deployed week 46?

g: yes, that could absolutely make sense. but i think that the graph is misleading then. i would prefer that it went down to 0 during week 5 instead of just omitting the data.

h: (laughs) i agree. it would make more sense if this was about volume, like how many jira ids are deployed over a period of time. if it was deployment frequency, then every week should be shown in the x axis. it's a strange graph, and maybe that should be improved, and visualize the data in another way.

g: yes, because you can see on week 4, the reason why we reached 20 is because it had been 5 weeks since the previous release.

h: yes, makes sense.

g: so actually the lower deployment frequency you have, the higher the spikes would be in this chart.

h: yes.

h: it's at least interesting to look at, and you gave some input. so if we look at lead time for change (shows report), this one says that the average is 13 almost 14 days, does that make sense to you? that it's how long it takes from code committed to code successfully running in production?

g: yes, it kind of aligns with what i asid before, that we release twice a month, so that's every fourteenth day, so that sounds reasonable to me.

h: then at least, we can say that it kind of reflects reality to some extent, maybe not for every part of the year, but at least for a totality it's not that far away.

g: no, i mean for some features, we had features that stay in PRs for months because of what i told you before that we kind of open a PR quite early, so when those features show up, that will create spikes in this diagram. so i think it makes sense that we have a couple of those spikes, and the median is lower.

h: that explains the spikes, that's really good.

h: those are the questions i had, and you mentioned factors that may impact deployment frequency and lead time. you spoke about the graphs. so thanks for participating, it was very insightful, and you gave good answers, and i will take this, use it, analyse it and so on. we also have one interview with team 1, and we will see what they say. they have quite a good structure and they deploy once a week. almost no teams look at this data except for one team. almost all teams say that they don't understand it, or they don't see any value in it, it doesn't apply to them, it doesn't reflect reality and so on.

g: maybe it's easier for an enabler team. for it to work, you have to have a continuous delivery approach, and many consumer teams don't have that, so maybe this becomes more important, because the data will always be dependent on other stuff that are not in the control of only the developers. like, when a feature is ready, it won't reach production, it might be stuck in two weeks from the time that it's ready to the time it's in rpoduction because it needs translations.

h: yes, i see totally what you are saying, and that is maybe the problem. maybe that's the interesting data, the time from it being developed until the time it's being ready, ideally you would want to measure the time which you can control, because that's what you can impact.

g: yes. and currently, the workflows don't differnetiate if it's a draft pr or a real pr, so maybe we shouldn't send the first ocmmit if the pr is a draft, but only when the draft pr is converted t oa regular pr. in our team it makes sense, because a draft pr is very unready.

h: thank you, it was a pleasure to talk to you!
