# lunch-buddy

## Slack Install
1. First thing you need to get the slack bot working is a slack API token unique to your workspace. To obtain this you'll need admin access and will go to <https://api.slack.com/apps/> and click create new app. From here click the second option for create from manifest and paste the app manifest in there.

![Build App Options](/docs/BuildAppView.png)


2. Now that our app is created the next step is to install it to our slack workspace. So when you first open the app you'll see options to install the app and you'll want to select to install it to the SEC workspace. 

![Post Create App Options](/docs/PostCreationView.png)


3. Another important key (since I spent so much time on the dwight shrute quotes) You'll want to scroll to the bottom of the basic information to *Display Information* and yuo can edit the display information. 

![Slack Bot Display Info](/docs/DisplayInformation.png)

This is the user MALs will see in their lunch buddy pairing and you can add an icon (I suggest Dwight Schrute on the desk in season 5 Episode 13)


4. Once it's installed you'll want to go to *Install App* on the left side

![Install App](/docs/SlackInstallApp.png)

Then click Copy to copy your API token and you'll need it in the next step for AWS.

5. Create both the lunch_buddy and archive channels, these can be named whatever you want but make sure the archive channel is private. You'll also need to add the bot to this channel (just like a normal user). Remember the lunch_buddy channel is where the users we want to match will be and archive will be a vieew just for record keeping.

5. Now you need to get the Channel IDs from Slack for the archive channel and the lunch_buddies channel. To do this go to the Channel and click on it's name.

![Channel view](/docs/ChannelView.png)

From here you should see the channel ID at the bottom and copy that for both channels and you'll want to copy them for AWS.

![Channel Info](/docs/ChannelInfo.png)

## AWS Install
1. The code base is set up already on AWS lambda on the Internal Socials chair's aws account so year to year you should just have to change the env variables. The app is called lunchbuddy under the AWS lambda tab.

![AWS Lambda Functions](/docs/AWSLambdaFunctions.png)

Once you enter the lambda function you will click *configuration* and *Environment Variables*

![AWS ENV vars](/docs/ENVVARS.png)

2. From here get the API token from step 4 of the previous section and update it under *SLACK_TOKEN* and take the 2 channel ID's from step 5 in the previous section.

3. To set up the automation go to AWS EventBridge and click on *rules* on the left hand side and then the *monday-9am* rule we have in place. From here you can Enable and Disable the bot so it'll automatically run at 9am on monday.

![Toggle Event Bridge](/docs/Monday-9amRule.png)

4. Celebrate you're done! The bot should run at 9am every monday now :fireworks: :gift_heart: :sunglasses: