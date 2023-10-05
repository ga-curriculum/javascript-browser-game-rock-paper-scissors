# User Stories

A quick and easy way to think about the functionality of our application is through ************user stories.************ This will seem a little strange with an application this simple but thinking about the functionality we will need to support our user stories is a great way to approach our pseudocode.

<aside>
📚 User stories are short, informal descriptions of an aspect of an app’s functionality, written from the perspective of an end-user or stakeholder, which are used to communicate  requirements during software development.

</aside>

Here are the user stories for this application:

> As a user, I would like to see a selection of rock, paper, and scissors when I arrive on the page, so that I am able to select my weapon of choice against the computer player.
> 

> As a user, after I have made a selection I would like to know whether myself or the computer won, so that I am able to feel like I am better (or worse) than the machine.
> 

Note that our user stories are inherently non-technical! To construct these user stories we are viewing the functionality of this application **from the perspective of the user** (or other stakeholder). But by thinking about these user stories, we’re able to approach our pseudocode using a systematic approach.

## Anatomy of a User Story

Looking at our user stories above there is a clear pattern:

> As a user …
> 

This is the stakeholder statement - this describes who will be served by this user story. At this point in the course everyone that uses your app can broadly be described as a user, but as the course continues we’ll see stakeholders like, **************guests**************, ****************************************************users who created a resource****************************************************, even ************admins************.

<aside>
🧠 It is very common for us to abbreviate As a user as AAU.

</aside>

> I would like …
> 

Broadly, this is the feature request that should be implemented to satisfy the user. The feature described here should be a vertical slice of your application’s feature set. For example our second user story above indicates that after a selection has been made that the user should know whether they won or lost. This will require a little bit of logic behind the scenes that is invisible to the user, but will also result in a message displayed to the user as well. The user story encompasses all of those components in the goal of delivering a complete feature to the user.

> So that I …
> 

This describes the motivation behind the user story, and may be omitted if the reason is extremely obvious. 

<aside>
❓ Review the first user story above. Given this information, what are some pieces of code we might need to make this application work?

</aside>