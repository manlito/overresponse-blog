title: Added Survey Finished Event
date: 2014-04-24

We have added a new event that a host app can listen for when rendering OverResponse surveys. This new event type is the `onSurveyFinish` event. As its name implies, you can use it to tell when the user reaches the end of the survey.

Currently, the event data returned by this method is all the survey data. Also, this method could fire twice, if the user returns to previous to review previous answers.

There is one sample which was done to show how you can use events: [Survey events sample](http://docs.overresponse.com/demos/events). Please take note that in all survey events, there is no processing of the input given by the user. So, in case you plan to display it or send it to your server, this could be a potential source for random user input. 


