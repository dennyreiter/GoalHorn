# GoalHorn

This is a Node Red flow that uses  [JayBlackedOut's](https://github.com/JayBlackedOut/hass-nhlapi) goal sensor to trigger a light and play the team goal horn on a Google Home.

![Goalhorn Flow](NHL-goal-flow.png)


The flow triggers on the **nhl_goal** event.  I edited down goal horns I found on Youtube to be around 30 seconds and named each with the team_id that is sent by the event. To use the horns, put them in an accessible directory, I used my HA local directory, under audio/goalhorns.  To get the Google home to play them, I had to use my external URL, and I use [Nabu Casa](https://nabucasa.com/) for that (which works great, by the way and supports Home Assistant.)

You will also want to (unless you don't and you can remove it,) create an input_boolean helper in Home Assistant named **goal_horn**.  This way you can disable the flow in case you don't want your movie/sleep/etc interrupted.  There is a second, simple flow that I use that resets it to on at 9am every morning.  It's handy because if you are using Nabu Casa and exposing entities to Google, you can just say **"OK Google, turn off goal horn"** and it will stay off until the next morning.


I claim no copyright or ownership of the horn sounds, nor the music played with them.
