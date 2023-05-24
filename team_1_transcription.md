# Interview 3
## Conducted 20 april 2023

## Please explain your team structure.
We have a product owner, and then we have a SCRUM master. We have two, two and a half UX designers, and currently, I think we have six or seven developers. And we also have someone who focuses more on data, collecting data from the planner, etc.
As communication tools, we mostly use Slack and Teams (we use Teams for meetings), otherwise, we use Slack.

## Please briefly explain your work process from sprint planning to release.
We follow a mix of SCRUM and Kanban. We have two-week sprints, but we don't plan in detail how much we will accomplish in the sprints. Instead, we have a checkpoint every other week to discuss roughly what we think we will be able to achieve, and then we add it to the plan. So, we have a backlog from which we take items, and then we have two-week sprints. We release every week.
Previously, our releases were more spread out and tied to specific features being completed. But we found that sometimes there was a long gap between releases, so we decided to try releasing every week.
For major features, we use feature flags so that we can release them even if they are not fully completed. So, we release every week with bug fixes and partially completed work.

## How often do you aim to deploy to production?
We have covered this question earlier. Our goal is to deploy once per week, and we almost always achieve that. We deploy to a test environment where we can test it as closely as possible to the environment that will be used by the customers.
We also have a team-wide testing session every Monday for the items that will be released. If we don't find anything blocking, we release on Monday. If we discover a bug or something that needs to be fixed before the release, we address it first, and then we might release on Tuesday or, in some cases, Wednesday.

## How quickly do you wish the time to be from code commit to the code running in production (lead time for change)?
As mentioned earlier, for us, it is mostly within a week. However, for major features, they are released to production behind a feature flag, so the customers don't immediately have access to them. But for smaller items, the lead time is a maximum of one week.

## Do you regularly look at DORA metrics? How do you act accordingly? If not, what may be possible reasons for not looking at it?
We don't really look at DORA metrics. It was set up for our project by a separate DevOps team that is external to our team. They set it up for us, but our team has never really delved into it or examined the statistics. There isn't really a specific reason for it, mostly just a lack of knowledge. We haven't really taken the time to understand what it is and what data is being collected. It's something we should probably look into more, but it just hasn't happened yet.

## How do you explain your deployment frequency report? (show report)
It varies a bit, and there may be some inaccuracies in the statistics. I know that the DevOps team made some changes to our metrics scripts because they weren't showing the correct data before. Some things weren't included as they should have been, and that might be the reason for the discrepancies.
I don't have any other explanation for the differences.
Each Jira ID is linked to a specific task, and sometimes we don't link it if it's a minor fix, so we don't always have it connected to Jira. But the majority are probably linked there. These Jira tasks vary in size greatly.

## How do you explain your lead time for change report? (show report)
The average lead time is 8 days, which aligns with our weekly releases. However, for example, in week 31, the lead time was over 30 days, and that seems to be due to vacation time when we didn't release weekly. We had almost 4-5 weeks without any releases during everyone's vacations. During the summer and holidays, people tend to have shorter vacations. Maybe there is a week where we don't release, but it is more noticeable during the summer when people are on vacation for longer periods.
It's difficult to determine if the reports are accurate or if there was a misinterpretation in the scripts or changes made to the DORA statistics. We have been releasing weekly for quite some time.

## What are factors that may impact your deployment frequency?
As mentioned earlier, we usually release every week, except during vacations and similar circumstances. Changes to our DORA scripts can also have an impact. But apart from that, we typically release weekly.

## What are factors that may impact your lead time for change?
As mentioned earlier, we usually release every week, except during vacations and similar circumstances. Changes to our DORA scripts can also have an impact. But apart from that, we typically release weekly.