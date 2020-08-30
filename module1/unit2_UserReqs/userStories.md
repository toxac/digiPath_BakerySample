Sometimes you have a need to represent User Stories that describe a back end service, API, web service, or similar.

First of all, a couple of warnings.
1. Make sure that you’re not creating a “Technical Story”. Technical Stories are a misunderstanding of the User Story practice. See trap#5 here.
2. If your team regularly creates “back end service” stories, it is likely that your team could be a Component Team, and having too many component teams in an organization can greatly harm agility to the point that your organization operates more like waterfall than Agile. See this link for more on that subject: https://less.works/less/structure/feature_teams.html
3. If a single team feels the need to create both a “back end story” and a “front end story”, or anything similar to that (Technical Story + Business Story, etc), then you are likely implementing the User Story practice wrong. This is an indicator that you’re doing horizontal slicing instead of vertical slicing. See trap#5 here

The only time that a back end story is really a true user story, is when your team is a component team(your team can’t deliver an end to end user visible feature), OR when your team works on a product that is a web service or API that is sold or used outside of your company.

So, with all of those caveats, here is my advice for creating these kinds of stories.
1. The acceptance criteria should only describe the UI. Note that I didn’t say GUI — I said UI. The UI for your web service is it’s api or service signature. This typically includes input variables(payload), output variables, exceptions, and/or error codes. Describe this input/output data in business terminology whenever possible!
2. Avoid describing anything beyond the API in the user story, but do describe the logic of how the inputs are processed. Again, use business terminology, something a business user would understand, whenever possible.
3. These kinds of stories lend themselves quite nicely to acceptance criteria that are represented using the Specification By Example techniques (see the presentation link at top, page 26 and beyond in the PDF), since those always describe expected test inputs and expected test outputs. Further, you can slice these stories quite thin since you can use the various data scenarios to slice the story and still have end to end functionality(request/response) delivered.
4. In terms of identifying a user role or persona, it would be nice if you could refer to an end user of your service who is a human if at all possible. If you don’t have line of site to the real end user, you can always just refer to a user role of “API user” or something. But again, all of the above caveats apply.

Back End stories also mix nicely with this non traditional Agile User Story slicing model, as usually your system acts as both a downstream(request) and an upstream(response) system.