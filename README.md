# Initial State SmartThings SmartApp

This repository is a host of the Initial State Event Sender - a SmartThings SmartApp intended to make easy the process of sending events that ocur on a SmartThings network to Initial State for visualization.

The actual SmartApp code is inside the official [SmartThings Public](https://github.com/SmartThingsCommunity/SmartThingsPublic/blob/master/smartapps/initialstate-events/initial-state-event-streamer.src/initial-state-event-streamer.groovy) github repo. However, because of the way SmartThings does app aproval and deployment as well as the requirement for commit squashing, I wanted to keep the code in a separate repo as well to keep the git history. This way, any change in the official github repo can just be a copy and paste commit.

Additionally, you'll find un-official or do-it-yourself SmartApps in this repo like the unbuffered Initial State Event Sender (which is based on the original design of this app and is by its very nature much less complex and therefor less fragile in the SmartThings ecosystem).

##Installation


###Official Version
For the official version, you can install the SmartApp by following the SmartThings button in your [Initial State Account Settings](https://www.initialstate.com/app#/account) page.

###DIY Version

1. Copy the code from [`unbuffered-event-sender.groovy`](https://raw.githubusercontent.com/davidsulpy/initialstate-smartapp/master/unbuffered-event-sender.groovy)
2. Log in to ide.smartthings.com with your SmartThings account.
3. Navigate to My SmartApps
4. Select "New SmartApp"
5. Select "From Code"
6. Paste the code copied from the unbuffered-event-sender.groovy
7. Select "Create"
8. Edit line 162 and replace `YOUR_ACCESS_KEY` with an access key from your Initial State account. Optionally, you can edit the bucket information above this line should you wish.
9. Select "Save"
10. Select "Publish" -> "For Me"

Now switch to the SmartThings mobile app

1. Go to the Marketplace
2. Select the SmartApps tab
3. Select My Apps
4. Select the DIY Initial State Event Streamer
5. Configure the sensors and capabilities you'd like to monitor
6. Select Done

You should now be all set! Please note, however, that events will populate the bucket automatically as new events happen on your SmartThings network. Your history of events will build from when you setup the SmartApp forward, so, if you don't see any events in your Initial State bucket immediately, it's most likely because no events have occurred just yet!
