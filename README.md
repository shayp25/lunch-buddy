# lunch-buddy

## Slack Install
1. First thing you need to get the slack bot working is a slack API token unique to your workspace. To obtain this you'll need admin access and will go to <https://api.slack.com/apps/> and click create new app. From here click the second option for create from manifest and paste the app manifest in there.
![Build App Options](/docs/BuildAppView.png)


2. Now that our app is created the next step is to install it to our slack workspace. So when you first open the app you'll see options to install the app and you'll want to select to install it to the SEC workspace. 
![Post Create App Options](/docs/PostCreationView.png)


3. Another important key (since I spent so much time on the dwight shrute quotes) You'll want to scroll to the bottom of the basic information to *Display Information* and yuo can edit the display information. 
![Install App](/docs/DisplayInformation.png)
This is the user MALs will see in their lunch buddy pairing and you can add an icon (I suggest Dwight Schrute on the desk in season 5 Episode 13)


4. Once it's installed you'll want to go to *Install App* on the left side
![Install App](/docs/SlackInstallApp.png)
Then click Copy to copy your API token and you'll need it in the next step for AWS.

## AWS Instal
1. The code base is set up already on AWS lambda on the Internal Socials chair's aws account so year to year you should just have to change the env variables. The app is called lunchbuddy under the AWS lambda tab.
![Install App](/docs/AWSLambdaFunctions.png)
